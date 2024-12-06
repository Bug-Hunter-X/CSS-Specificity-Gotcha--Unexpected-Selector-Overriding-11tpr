# CSS Specificity Gotcha: Unexpected Selector Overriding

This repository demonstrates a subtle CSS specificity issue where a more specific selector is unexpectedly overridden by a less specific one.  The problem highlights the complexities of CSS specificity calculation, especially when dealing with nested selectors.

## Bug Description
The bug arises from the way the browser resolves conflicting CSS styles when multiple selectors target the same element.  A more specific selector (e.g., `.container .item.special`) is sometimes overridden by a less specific selector (e.g., `.item`) due to how specificity weights are calculated. 

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` (or create your own HTML file which includes the CSS).
3. Observe the background color of the `.item.special` element.  You'll likely see yellow instead of the intended lightpink.

## Solution
The solution involves understanding and adjusting the CSS selectors to ensure the intended specificity and style application.   The solution file (`bugSolution.css`) demonstrates how to correctly override conflicting styles.