Content Elements
################

The documents ":doc:`../../1-MakingWebAccessible/2-principles`" and
":doc:`1-four-easy-tips`" cover most of the accessibility issues you have to be
aware of as an editor. However, there are some TYPO3 Content Elements which
need some special attention:

Images
******

Under the tab "Images" there is a section called "Accessibility". This section
gives you all the fields which can be used for accessibility.

.. figure:: /Images/2-MakingTypo3Accessible/3-Editor/figure-2-3-1-1.png
      :align: center

      Figure 2-3-1-1: Images tab with Accessibility section

Alternative labels
  Insert alternative text for each image, one per line, describing the image,
  unless the image has no meaning. The alternative label is meant to be
  relatively short.
Titles
  The title attribute represents advisory information for the element, such as
  would be appropriate for a tooltip. On a link, this could be the title or a
  description of the target resource; on an image, it could be the image credit
  or a description of the image; on a paragraph, it could be a footnote or
  commentary on the text; on a citation, it could be further information about
  the source; and so forth. The value is text. Titles for images are not as
  important as the alternative labels. The accessibility of the title attribute
  has fallen victim to an unfortunate combination of poor browser support, poor
  screen reader support, and poor authoring practices. Never enter the same
  information in the alternative labels and the titles.
Long Description URLs
  In some instances, an image is too complex to describe in a few words.
  Charts and graphs are primary examples of such images. Although there does
  not appear to be any limit to the length of text in an alternative label,
  alternative text is meant to be relatively short, so it would be an abuse of
  this attribute to write more than a few words, or, at most, a few short
  sentences. The answer, then, is to provide a brief alternative text
  description of the image and then provide a longer description on a different
  page.

Images & Text
*************

See `Images`_.

Table
*****

The purpose of data tables is to present information in a grid, or matrix, and
to have column or rows that show the meaning of the information in the grid.
When screen readers read straight through data tables, especially large
ones, it's easy for users to get lost.

In order for a data table to be accessible, it must have the proper markup in
the HTML. When the proper HTML markup is in place, users of screen readers can
navigate through data tables one cell at a time, and they will hear the column
and row headers spoken to them.

Let's see what the accessibility section of the content element "Table" looks
like:

.. figure:: /Images/2-MakingTypo3Accessible/3-Editor/figure-2-3-1-2.png
      :align: center

      Figure 2-3-1-2: Table tab with Accessibility section

Table Caption
  Tables should have some sort of title or caption assigned to them. It is not
  absolutely necessary to have a caption on every data table for the sake of
  accessibility, but it is still a good practice.
Table Summary
  A table summary is not a requirement for simple tables, but can increase the
  comprehension of more complex tables for people using screen readers. For
  instance you can highlight the important elements of a table, and help the
  user to know what to look for in the data.
Use Table Footer
  The table footer element is used to mark up a table footer, such as a total
  row. Not using a table footer is not an accessibility issue. It can help
  highlight important information.
Table Header Position
  The very first step toward creating an accessible data table is to designate
  row and/or column headers.
No CSS styles for this table
  Not accessibility related
Additional CSS Class
  Not accessibility related

File Links
**********

Depending on the the "Layout" setting, which you can find in the "Appearance"
tab, a preview or icon will be shown in front of a file link. This is an image.
Images need an alternative label, as described in `Images`_, unless the image has
absolutely no meaning. TYPO3 will fill the alternative label automatically,
unless you override it with the field "Alternative Labels for icons/thumbnails"
in the "General" tab.

Menu/Sitemap
************

For navigation items it is important to identify the menu with a title. The
title will tell the visitor of the site what the menu is all about. If the menu
is not relevant to the visitor, it also needs the possibility to skip the menu.

These issues are covered in the "Accessibility" section in the "General" tab.

.. figure:: /Images/2-MakingTypo3Accessible/3-Editor/figure-2-3-1-3.png
      :align: center

      Figure 2-3-1-3: Accessibility section

Menu block title
  The title will give the visitor information about the navigation item, like
  "Main navigation" or "Upcoming events".
Add link to bypass navigation block
  This will add a link on top of the menu/navigation to skip this item and
  move on to the next part.
Link text to bypass navigation block
  When empty TYPO3 will use default text for the link to bypass the navigation
  block, like "Skip navigation". You can override the default text here.