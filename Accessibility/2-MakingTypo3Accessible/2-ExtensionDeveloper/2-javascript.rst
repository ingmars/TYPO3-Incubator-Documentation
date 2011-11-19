Javascript
##########

JavaScript allows developers to add increased interaction, information
processing, and control in web-based content. JavaScript can also cause
accessibility problems by limiting navigation using a keyboard or assistive
technology, presenting content or functionality that is not accessible to
assistive technologies, limiting user control over automated content changes,
and modifying the normal functionality of the browser.

When faced with JavaScript accessibility issues, you must do one of the
following:

- Ensure the JavaScript is directly accessible
- Provide an accessible, non-JavaScript alternative

JavaScript is often used to make cosmetic or other content changes that do not
affect accessibility. Content written to the page using JavaScript is
accessible if:

- Device independent event handlers are used.
- JavaScript enabled content and functionality is accessible to assistive
  technologies.
- Scripted pages and elements are navigable using a keyboard.
- The normal browser functionality is not modified in a way that may cause
  confusion or inaccessibility.
- An accessible alternative is provided when JavaScript cannot be made
  natively accessible.

Should I use JavaScript at all?
*******************************

Of course you should! Imagine a Web 2.0 website without JavaScript. Most
assistive technologies know how to handle JavaScript. WAI-ARIA especially helps
with dynamic content and advanced user interface controls developed with Ajax,
HTML, JavaScript, and related technologies.

JavaScript Alternatives
***********************

There are many ways to provide alternatives to JavaScript. Newer versions of CSS
allow much of the behavior of JavaScript to be replicated using CSS alone.
Drop-down menus, navigation bars, and interactive images can all be developed
without relying on JavaScript. However, the implementation of CSS across
browsers and assistive technologies is varied and problematic. When JavaScript
itself cannot be made natively accessible, you must provide an accessible
alternative. This can be done by replicating or replacing the JavaScript
behavior with server-side processing. You can also provide <noscript> content
which will be accessible when JavaScript is disabled or not available to the
end user.