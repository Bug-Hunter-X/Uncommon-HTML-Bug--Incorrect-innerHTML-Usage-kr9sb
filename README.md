# Uncommon HTML Bug: Incorrect innerHTML Usage

This repository demonstrates an uncommon bug related to the use of `innerHTML` in HTML.  Improper usage of `innerHTML` with multiple elements can lead to unexpected results and security vulnerabilities.

## Bug Description
The `innerHTML` property can be dangerous if the content comes from an untrusted source, because it can introduce cross-site scripting (XSS) vulnerabilities. Even when the source is trusted, using `innerHTML` to inject multiple elements may not produce the intended layout or may result in unexpected behavior due to the browser's rendering engine.

## Bug Solution
The correct solution involves using `document.createElement` to create individual elements and then appending them to the parent node, which allows for better control and avoids potential XSS vulnerabilities.  This method provides better separation of concerns and improved security and maintainability.
