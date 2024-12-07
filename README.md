# CSS ':first-of-type' Selector Bug

This repository demonstrates a subtle bug related to the CSS `:first-of-type` pseudo-class selector.  The issue arises when a paragraph element, targeted by the selector, has whitespace-only text nodes (text nodes containing only spaces, tabs, or newlines) before or after the actual visible text content.  This can cause the selector to fail to match the intended element in some browsers.

The `bug.css` file contains the problematic CSS code, and `bugSolution.css` provides a solution to address this issue.

## Bug Description
The `:first-of-type` selector is intended to select the first element of its type within its parent. However, whitespace-only text nodes can interfere with this functionality, preventing the selector from properly identifying the first visible paragraph.

## Solution
The solution utilizes more robust techniques to target the first paragraph, ensuring that whitespace-only text nodes do not affect the selection.

## How to reproduce the bug
1. Create an HTML file with the structure similar to what is described in the `bug.html` file.
2. Include the `bug.css` stylesheet in the HTML file.
3. Observe the styling of the paragraphs. The first paragraph may not be styled as expected if there are whitespace-only text nodes surrounding the visible text.