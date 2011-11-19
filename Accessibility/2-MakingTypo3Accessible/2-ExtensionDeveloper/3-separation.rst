Always separate style from content
##################################

HTML tags should never be used to apply presentation – that’s the job of CSS
(Cascading Style Sheets).

Unless you’ve had to interact with HTML markup through media other than your web
browser, it doesn’t seem obvious to imagine that your web pages have a life
outside the browser window, but they very often do. Web pages can be consumed
by humans and machines in many different ways!

When you separate visual aspects (i.e. style) from the actual meaning of a
document, you end up with a document that always means the same thing. The way
it’s presented or consumed can vary. One common technique web designers use is
to apply different style sheets for different media. For example, you can apply
a certain stylesheet only when a document is printed to paper, another one when
it’s viewed on screen, and yet another when it’s accessed by a text-to-speech
aural browser.

A text-to-speech reader also understands the tags <strong> or <em> but it treats
text output with those tags very differently from the way a visual browser
responds. The TTS reader adjusts vocal tone or volume, rather than contrast or
text style, which conveys the same meaning but through a different medium.

Avoid Inline Styles
*******************

An inline style loses many of the advantages of style sheets by mixing content
with presentation. It is mostly used when you want to apply a formatting style
to single element within a web page. Because they are the most specific in the
cascade, they can override things you didn't intend them to and can't be
overriden unless you use the !important attribute. Inline styles are hard to
maintain.

.. note::

   Some governmental accessibility guidelines like the Dutch "Webrichtlijnen"
   don't allow inline styles at all

The TYPO3 core offers a method to put inline styles in a temporary external
stylesheet. Instead of writing

::

   <div style="width: 200px;">Content</div>

you can use the following in your extension

::

   $plugin = 'tx_yourplugin.';
   $selector = '.width200';
   $declaration = 'width: 200px;';

   $GLOBALS['TSFE']->tmpl->setup['plugin.'][$plugin]['_CSS_PAGE_STYLE'][$selector] = $selector . ' { ' . $declaration . ' }';

This will add an extra line to the temporary stylesheet of the page. This
temporary stylesheet "/typo3temp/stylesheet_xxx.css", where xxx is a hash
string, is mostly the same for every page. When extra styles are added for a
single page, the stylesheet will be written with these additions and will get
another name, by using a different hash string.

Your container can now use a class for the width

::

   <div class="width200">Content</div>

