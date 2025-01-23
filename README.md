# Uncommon HTML DOM Manipulation Bug

This repository demonstrates a subtle bug in HTML and JavaScript related to DOM manipulation.  Specifically, it highlights the error that occurs when trying to access a DOM element after it's been removed.

## Bug Description

The `bug.html` file contains JavaScript code that attempts to remove a div element and then modify its style.  This is incorrect, because once `remove()` is called, the element no longer exists in the DOM.  The subsequent attempt to access its style will throw an error.

## Solution

The `bugSolution.html` file shows the correct way to handle this scenario by only using either `remove()` or modifying the style before removing the element.  Note that using `display: none;` will hide the element but will still allow you to get it by Id later.