Semantics
#########

Anyone who creates their own HTML pages today should aim to make their markup
semantically correct.

What is Semantic HTML?
**********************

Semantics is the study of meaning: how meaning is created and applied to signs.
"Why does X mean X?" is a question of semantics.

HTML is the markup language that we use to write web pages. It’s understood by
standard web browsers, as well as dozens of other types of "user agents",
including mobile phones, search engine spiders, aural browsers etc.)

HTML consists of two types of things:

- Tags
- Text content

A few tags can provide content on their own (like images, Flash movies, or metadata),
but most HTML tags are used to apply structure to content.

Semantic HTML, or "semantically-correct HTML", is HTML constructed in such a way that
the tags used to structure content are selected and applied appropriately to the
meaning of the content.

For example, if you’re wanting your HTML to be semantically-correct

- A <p></p> paragraph tag pair should only be used to indicate a paragraph
  (which is a structural concept). It should never be used to apply space to a
  web page. Never, ever, use a series of <p> tags to create space!
- The HTML tags <b></b> (for bold), and <i></i> (for italic) should never be
  used, because they define formatting, not the meaning or structure of the content.
  Instead, use the replacements <strong></strong> and <em></em> (meaning emphasis),
  which by default will turn text bold and italic (but may not do so in all
  browsers), while also adding meaning to the content.

Ease of use
***********

First of all, semantic HTML is clean HTML. It’s much easier to read and edit
markup that’s not littered with extra tags and inline styling. Clean markup
also saves time and money when other people have to interact with it, such as
when a web developer has to implement your page template in a content management
system or any other web application.

Another benefit is that your HTML files are also smaller and load faster.