# SC1-4-3-main-text-bg-contrast

## Description
This test checks that the main body of text content on a page contrasts sufficiently with the background, gradient or image behind it.


## Background

- [Understanding SC 1.4.3](https://www.w3.org/TR/2014/NOTE-UNDERSTANDING-WCAG20-20140311/visual-audio-contrast-contrast.html)


## Assumptions
- It is possible to determine what is the main body of text
- The text is not an image
- It is possible to determine the text colour
- It is possible to determine the colours behind the text


## Test properties
| Properties        | Values
|-------------------|-----------
| Test name         | Main-text - background contrast
| Success criterion | 1.4.3 Contrast minimum
| Test mode         | Automatic / Manual
| Test environment  | DOM + CSS, Rendered page
| Test Subject      | Web page state
| User profile      | Requires sight


## Test procedure


### Selector
Test method: [automatic][earl:automatic]

Look at each text containing element within the main content container that is not empty.
eg. body > main > (h*/p/li/label/span/div etc)


### Step 1
Test method: [automatic][earl:automatic]

For each text element:

- determine if a text colour is set.
- determine if the parent background colour is set.
- determine if the parent element or another element sits immediately behind the text.
- determine if the parent or other element has a background colour/gradient/image.
- determine if the text has a border or shadow set.
- calculate the text height to determine the contrast required.


### Step 2
Test method: [automatic][earl:automatic]

For each text element:

- compare the text colour with the parent background colour (if either does not exist, fail).
- if needed, compare the text colour with the other element background colour.
- if there is a gradient, determine if lightest shade is above/below/left/right of text and compare background above/below or left/right or text with text colour.
- if text has a border and/or shadow, determine width of border/shadow above/below/left/right of text, and if any are all are 1px or greater compare text colour with border/shadow colour.

### Step 3
Test method: [manual][earl:manual]

For each text element:

- if an image is immediately behind text, with no border/shadow/gradient-layer, a manual test will be required.



[earl:automatic]: pages/test-modes.md#automatic
[earl:manual]:  pages/test-modes.md#manual