# Uncommon HTML Bug: Display Style and innerHTML Update Timing

This repository demonstrates an uncommon bug related to the timing of updating an HTML element's display style and its innerHTML.  The issue arises when attempting to hide an element using `style.display = "none"`, then immediately changing its `innerHTML`.  Due to the asynchronous nature of JavaScript, the browser might render the `innerHTML` change briefly before the display style is applied, causing a visual flicker.

## Bug Description

The `bug.html` file contains a simple HTML page with a div and a button. Clicking the button hides the div and then updates its content.  The timing between these two actions is incorrect, leading to a visual glitch.

## Solution

The solution (`bugSolution.html`) addresses this issue by adding a small delay using `setTimeout` to ensure the display style is updated before the `innerHTML` is modified.