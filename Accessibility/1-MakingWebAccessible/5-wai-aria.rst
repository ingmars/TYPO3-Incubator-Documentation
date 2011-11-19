WAI-ARIA
########

WAI-ARIA, the Accessible Rich Internet Applications Suite, defines a way to make
Web content and Web applications more accessible to people with disabilities. It
especially helps with dynamic content and advanced user interface controls
developed with Ajax, HTML, JavaScript, and related technologies. Currently
certain functionality used in Web sites is not available to some users with
disabilities, especially people who rely on screen readers and people who cannot
use a mouse. WAI-ARIA addresses these accessibility challenges, for example, by
defining new ways for functionality to be provided to assistive technology. With
WAI-ARIA, developers can make advanced Web applications accessible and usable to
people with disabilities.

ARIA isn't part of HTML5; it's a specification written by the W3C, and uses
attributes rather than elements, as it's designed to supplement any markup
language, not just HTML. It can also be used with SVG, Adobe's MXML, and other
markup languages.

Adding ARIA information to HTML4 helps accessibility, but the HTML document will
no longer validate. Because HTML5 is still in development, ARIA attributes will
validate in HTML5. Not only that, there are certain correspondences between the
two specifications in the HTML5 spec; some elements have built-in ARIA roles that
can't be overridden.

.. note::

   The Protocols and Formats Working Group (PFWG) published WAI-ARIA 1.0 as a
   W3C Candidate Recommendation on 18 January 2011

Making Ajax and Related Technologies Accessible
***********************************************

Web sites are increasingly using more advanced and complex user interface
controls, such as tree controls for Web site navigation. To provide an
accessible user experience to people with disabilities, assistive technologies
need to be able to interact with these controls. However, the information that
the assistive technologies need is not available with most current Web
technologies.

Another example of an accessibility barrier is drag-and-drop functionality that
is not available to users who rely on a keyboard only and cannot use a mouse. Even
relatively simple Web sites can pose challenges if keyboard navigation requires
many keystrokes.

Many Web applications developed with Ajax, DHTML, and other technologies pose
additional accessibility challenges. For example, if the content of a Web page
changes in response to user actions or makes use of time-based or event-based
updates, that new content may not be available to people who are blind or
people with cognitive disabilities who use a screen reader.

WAI-ARIA addresses these accessibility challenges by defining how information
about this functionality can be provided to assistive technology. With WAI-ARIA,
an advanced Web application can be made accessible and usable to people with
disabilities.

Technical Solutions
===================

More specifically, WAI-ARIA provides a framework for adding attributes to
identify features for user interaction, how they relate to each other, and their
current state. WAI-ARIA describes new navigation techniques to mark regions and
common Web structures as menus, primary content, secondary content, banner
information, and other types of Web structures. For example, with WAI-ARIA,
developers can identify regions of pages and enable keyboard users to easily
move among regions, rather than having to press Tab many times.

WAI-ARIA also includes technologies to map controls, Ajax live regions, and
events to accessibility application programming interfaces (APIs), including
custom controls used for rich Internet applications. WAI-ARIA techniques apply
to widgets such as buttons, drop-down lists, calendar functions, tree controls
(e.g. expandable menus), and others.

WAI-ARIA provides Web authors with the following:

- Roles to describe the type of widget presented, such as "menu," "treeitem," "slider," and "progressmeter"
- Roles to describe the structure of the Web page, such as headings, regions, and tables (grids)
- Properties to describe the state widgets are in, such as "checked" for a check box, or "haspopup" for a menu.
- Properties to define live regions of a page that are likely to get updates
  (such as stock quotes), as well as an interruption policy for those updates.
  For example, critical updates may be presented in an alert dialog box, and
  incidental updates occur within the page
- Properties for drag-and-drop that describe drag sources and drop targets
- A way to provide keyboard navigation for the Web objects and events, such as those mentioned above
