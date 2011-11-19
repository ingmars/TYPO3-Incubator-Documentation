Preliminary Review
##################

A preliminary review can quickly identify some accessibility problems on a Web site. A preliminary review does not check every accessibility issue and will not catch all of the problems on a site. Thus the method described in this page is not sufficient to determine if a Web site completely conforms to Web accessibility guidelines.

A preliminary review combines some manual checking of representative pages on a Web site, along with the use of several semi-automatic accessibility evaluation tools.

Select a representative page sample
***********************************

From the Web site to be reviewed, select a representative sampling of pages that match the following criteria:

- Include all pages on which people are more likely to enter your site ("welcome page", etc.).
- Include a variety of pages with different layouts and functionality, for example:

  - Web pages with tables, forms, or dynamically generated results;
  - Web pages with informative images such as diagrams or graphs;
  - Web pages with scripts or applications that perform functionality.

Examine pages using graphical browsers
**************************************

Use a graphical user interface (GUI) browser (such as Firefox, Internet Explorer, Netscape Navigator, Opera, Safari, or others) and examine the selection of pages while adjusting some settings in your browser or operating system as follows (some of these manual checks may require additional software):

#. Turn off images, and check whether appropriate alternative text for the images is available.
#. Turn off the sound, and check whether audio content is still available through text equivalents.
#. Use browser controls to vary font-size: verify that the font size changes on the screen accordingly; and that the page is still usable at larger font sizes.
#. Test with different screen resolution, and/or by resizing the application window to less than maximum, to verify that horizontal scrolling is not required (caution: test with different browsers, or examine code for absolute sizing, to ensure that it is a content problem not a browser problem).
#. Change the display color to gray scale (or print out page in gray scale or black and white) and observe whether the color contrast is adequate.
#. Without using the mouse, use the keyboard to navigate through the links and form controls on a page (for example, using the "Tab" key), making sure that you can access all links and form controls, and that the links clearly indicate what they lead to.

.. note::

   Browser extensions and other plug-in evaluation tools (such as AIS Toolbar
   for Internet Explorer and Opera, WAVE Toolbar for Firefox, Internet Explorer,
   and Netscape Navigator, or Web Developer Extension for Firefox) provide
   functionality to help perform many of these manual checks.

Examine pages using specialized browsers
****************************************

Use a voice browser (such as Home Page Reader) or a text browser (such as Lynx) and examine the selection of pages while answering these questions:

#. Is equivalent information available through the voice or text browser as is available through the GUI browser?
#. Is the information presented in a meaningful order if read serially?

.. note::

   Experienced users of screen readers may substitute a screen reader for a
   voice or text browser, but if blind, may need a sighted partner to compare
   information available visually; if sighted, listen to it with eyes closed,
   then open eyes and confirm whether the information is equivalent.

Use automated Web accessibility evaluation tools
************************************************

Use at least two automated Web accessibility evaluation tools to analyze the selection of pages and note any problems indicated by the tools.

.. note::

   These tools will only check the accessibility aspects that can be tested
   automatically, the results from these tools should not be used to determine
   a conformance level without further manual testing.

Summarize obtained results
**************************

Summarize results obtained from previous four tasks:

#. Summarize the types of problems encountered, as well as positive aspects that should be continued or expanded on the site.
#. Indicate the method by which problems were identified, and clearly state that this was not a full conformance evaluation.
#. Recommend follow-up steps, including full conformance evaluation which includes validation of markup and other tests, and ways to address any problems identified.
