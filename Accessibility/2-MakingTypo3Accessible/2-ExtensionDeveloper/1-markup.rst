Markup
######

One of the first ground rules of web design and development is to have proper
markup of the output according to its technology specification. Technology
specifications define the meaning and proper handling of features of the
technology. Using those features in the manner described by the specification
ensures that user agents, including assistive technologies, will be able to
present representations of the feature that are accurate to the author's intent
and interoperable with each other. This technology specification is mostly set
by the document type declaration.

WCAG 2.0 is a recommendation, and only describes HTML 4.01 and XHTML 1.0. HTML
4.01 is the latest mature version of HTML, which provides specific
accessibility features and is widely supported by user agents. XHTML 1.0
provides the same features as HTML 4.01, except that it uses an XML structure,
and has a more strict syntax than the HTML structure. WCAG 2.0 does not support
later versions of these technologies, because they are not considured mature
and/or are not widely supported by user agents. This includes XHTML 1.1 and
HTML5.

HTML5 is still a draft, and it will probably be quite some time before it
progresses to a recommendation. XHTML 1.1, has been a recommendation since 2001,
and got a second revision in 2010. It seems W3C thinks this specification is still
not well-supported enough by user agents.

However, this does not mean you can't use these specifications. HTML5 was designed
with better semantics and accessibility in mind.

Document Type Declaration
*************************

Although the DTD is configurable in TYPO3, the core did not care about proper
markup until version 4.7. To be more specific, all output was XHTML. Void tags,
like img, input, br and hr, always got their closing slash, even when the DTD
was specified as HTML 4.0 Transitional, which is actually the default doctype of
TYPO3.

No config.doctype set: HTML 4.0 Transitional:

::

   <img src="myimage.jpg" alt="My Image" />

which should be:

::

   <img src="myimage.jpg" alt="My Image">

Also attributes did not follow the rules of a Document Type. For instance, the
target attribute is not allowed for most of the XHTML specifications, except
XHTML 1.0 Frameset, but was added nevertheless.

When writing accessible extensions, you need to be aware of this topic! The
markup should completely comply with the DTD.

Templating
==========

Most extensions come with predefined (X)HTML templates. The extension
developer decides what specification will be applied to this template and most
of the time this will be XHTML.

With HTML5 being promoted lately, you might want to consider delivering templates
in multiple document types, so you can take full advantage of the HTML5
semantics. This will help the TYPO3 integrator when he does not need to
change the markup of your template, because the DTD he has chosen for the website
does not comply with your extension template DTD.

To check the config.doctype setting in TypoScript, you can use:


::

   TSFE:config|config|doctype

This will give you the value entered in config.doctype. You can check it by
using conditions, if statements or a case.

When using target attributes in TypoScript, you can check if the DTD allows for
frames.

::

   TSFE:dtdAllowsFrames

This will return TRUE or FALSE.

Coding
======

The TYPO3 core does not use templates for frontend output. All (X)HTML is
generated in PHP. This also happens frequently in extensions, because some issues
can't be solved with templates.

The settings above can also be used in PHP:

::

   $GLOBALS['TSFE']->config['config']['doctype']
   $GLOBALS['TSFE']->dtdAllowsFrames

It will return the same values as mentioned above.
