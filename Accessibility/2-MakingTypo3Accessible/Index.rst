Making Your TYPO3 Website Accessible
####################################

Making a website accessible can be simple or complex, depending on many factors
such as the type of content, the size and complexity of the site, and the
development tools and environment.

Many accessibility features are easily implemented if they are planned from the
beginning of website development or redesign. Fixing inaccessible websites
can require significant effort, especially sites that were not originally
"coded" properly with standard (X)HTML markup, and sites with certain types of
content such as multimedia.

Since TYPO3 4.7, the content elements of css_styled_content (except FORM and SEARCH)
have been adapted to use proper markup no matter what doctype has been selected. For
example, void (i.e. self-closing) tags will include the closing slash when an XHTML
doctype is in use but will not when an HTML doctype is used. Attributes are only
used when they are allowed by the doctype.

This document will describe some ways to help integrators, extension
developers and editors meet the accessibility guidelines.

.. toctree::
   :maxdepth: 2

   2-ExtensionDeveloper/Index
   3-Editor/Index