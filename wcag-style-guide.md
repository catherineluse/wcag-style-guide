# Accessibility Style Guide

Adapted from the [WCAG 2 A and AA Checklist | Usability & Web Accessibility](https://usability.yale.edu/web-accessibility/articles/wcag2-checklist)

# HTML Tags
[1.3.1 Info and Relationships (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships)
* Use semantic markup to designate headings, lists, figures, emphasized text, etc.
* Organize pages using properly nested HTML headings.
* Use ARIA landmarks and labels to identify regions of a page.
* When the appearance of text conveys meaning, also use appropriate semantic markup.
* [2.4.2 Page Titled (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/page-titled)
* Make sure each web page has a title tag that is descriptive, informative, and unique.
* [4.1.1 Parsing (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/parsing)
* Validate all page HTML, and avoid significant validation / parsing errors.
* [4.1.2 Name, Role, Value (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/name-role-value)
* Use ARIA to enhance accessibility only when HTML is not sufficient. Use caution when providing ARIA roles, states, and properties.

# Layout
## Do’s
[1.3.2 Meaningful Sequence (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/meaningful-sequence)
* Ensure that the source order presents content meaningfully. When the page is viewed without styles, all content on the page should still appear in a meaningful and logical order.
* [1.3.4 Orientation (AA) (2.1) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/orientation)
* All content and functionality should be available regardless of whether a mobile device is oriented vertically or horizontally, unless the orientation of the device is absolutely essential.
* [1.4.10 Reflow (AA) (2.1) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/reflow)
* Provide responsive stylesheets such that content can be displayed at 320px wide without horizontal scrolling. (Content which must be displayed in two dimensions, such as maps and data tables, may have horizontal scrolling.)
* [2.4.6 Headings and Labels (AA) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/headings-and-labels)
* Ensure that on each page, headings, landmark labels, and form labels are unique unless the structure provides adequate differentiation between them.

## Don’ts
* Avoid using whitespace characters for layout purposes.

# Navigation
[2.4.5 Multiple Ways (AA) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/multiple-ways)
* Each website should include at least two of the following: a list of related pages; table of contents; site map; search; or list of all pages.
* [3.2.3 Consistent Navigation (AA) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/consistent-navigation)
* When components are repeated across web page, they should appear in the same relative order with regard to other repeated components on each web page where they appear.
* When a navigation menu is presented on multiple pages, the links should appear in the same order on each page.

# Links and buttons
## Do’s
* Minimize the number of adjacent links to the same destination by combining adjacent images and text into a single link.
* Links should always be easily identifiable through non-color means, including both default and hover states. The easiest and most conventional way to signify links is underlining.
* [2.4.4 Link Purpose (In Context) (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/link-purpose-in-context)
* The purpose of each link can be determined from the link text alone, or from the link text and the containing paragraph, list item, or table cell, or the link text and the title attribute.
* If the visible text alone is not sufficient to convey meaning, use advanced techniques to provide additional meaning, such as ARIA attributes, screen reader only text, or the title attribute.
* If an image or icon is used as a button or link, the image has a text alternative sufficient to describe the purpose of the button or link.

## Don’ts
* Do not convey information solely through icons or symbols.
* Avoid emulating links and buttons. Use the a and button tags appropriately. 
* Avoid using a tags for buttons. 
* Avoid using div, span, etc. tags for links or buttons.


# Keyboard Navigation
## Do’s
* All functionality should be available to a keyboard without requiring specific timing of keystrokes, unless the functionality cannot be provided by a keyboard alone.
* Make sure the user can move focus to and from all focusable elements using a keyboard only.
* [2.4.1 Bypass Blocks (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/bypass-blocks) Provide a link to skip to the main content as the first focusable link on the page.
* [2.4.7 Focus Visible (AA) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/focus-visible) Provide keyboard focus styles that are highly visible, and make sure that a visible element has focus at all times when using a keyboard. 
* When inserting content into the DOM, insert the content immediately after the triggering element, or use scripting to manage focus in an intuitive way. When triggering dialogs and menus, make sure those elements follow their trigger in the focus order in an intuitive way. When content is dismissed or removed, place focus back on the trigger.
* Create a logical tab order through links, form controls, and interactive objects. 

## Don’ts
* [2.1.2 No Keyboard Trap (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/no-keyboard-trap)
* Ensure keyboard focus is never trapped on an element without an obvious way to move focus out of the element. 
* [2.4.3 Focus Order (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/focus-order)
* Avoid using tab index values greater than 0.
* Do not rely on browser default focus styles.

# Forms
[1.3.5 Identify Input Purpose (AA) (2.1) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose)
* If a form field asks for information about the user and if there is an appropriate HTML autocomplete attribute, include that autocomplete attribute.
* Programmatically indicate required fields using the required or aria-required attributes. Also, visually indicate required fields in the form’s instructions or form labels. Do not indicate required fields for CSS alone.
* Provide text instructions at the beginning of a form or set of fields that describes the necessary input.
* When providing inline help text, use aria-describedby to associate the help text with the input.

# Colors and Contrast
## Do’s
[1.4.1 Use of Color (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/use-of-color)
* Required fields and fields with errors must include some non-color way to identify them.
* When the color of words, backgrounds, or other content is used to convey information, also include the information in text.
* [1.4.11 Non-text Contrast (AA) (2.1) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast)
* Color contrast for graphics and interactive UI components must be at least 3:1 so that different parts can be distinguished.
* When providing custom states for elements (e.g. hover, active, focus), color contrast for those states should be at least 3:1.

## Don’ts
[1.3.3 Sensory Characteristics (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/sensory-characteristics)
* Do not identify content based on its color, size, shape, position, sound, or other sensory characteristics.

# Text
## Do’s
* Define texts and text containers in relative units (percents, ems, rems) rather than in pixels.
* [1.4.3 Contrast (Minimum) (AA) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum)
* Text (including images of text) have a contrast ratio of at least 4.5:1. For text and images of that is at least 24px and normal weight or 19px and bold, use a contrast ratio that is at least 3:1.
* [1.4.4 Resize text (AA) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/resize-text)
* Ensure that there is no loss of content or functionality when text resizes.

## Don’ts
[1.4.12 Text Spacing (AA) (2.1) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/text-spacing)
* Avoid using pixels for defining the height and spacing (e.g. height, line height, etc) of text boxes.
* [1.4.5 Images of Text (AA) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/images-of-text) Avoid images of text, except in cases such as logos.

# Images
## Do’s
[1.1.1 Non-text Content (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/non-text-content)
* All img tags must have alt attributes. 
* If short alt text is sufficient to describe an image, provide the short text via the image’s alt attribute.
* If a short text alternative is not sufficient to describe an image (such as in a chart, graph, or diagram), provide short text via the image’s alt attribute, and include a long description in nearby text.
* Images that are decorative, used for formatting, or contain content already conveyed in text have a null alt attribute or are implemented as CSS background images.

## Don’ts
Avoid images of text.

# Labels
## Do’s
[2.5.3 Label in Name (A) (2.1) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/label-in-name)
* The accessible name for a UI element must contain any visual label for the element. Accessible names for UI elements should match visual labels as closely as possible.
* When a visual label is present for an interactive element (e.g. link or form control), the accessible name of the element should contain the visual label.
* [3.2.4 Consistent Identification (AA) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/consistent-identification)
* When components have the same functionality across several web pages, the components are labeled consistently on each page.
* [3.3.2 Labels or Instructions (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/labels-or-instructions)
* Use semantic, descriptive labels for inputs. Visually position labels in a consistent way that makes associating labels with form controls easy. 

## Don’ts
Do not rely on placeholder text in lieu of an HTML label.

# Audio
[1.2.1 Audio-only and Video-only (Prerecorded) (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/audio-only-and-video-only-prerecorded)
* For pre-recorded audio (without video), provide a descriptive transcript that includes dialogue and all other meaningful sound.
* [1.2.2 Captions (Prerecorded) (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/captions-prerecorded)
* Provide captions for prerecorded audio content in non-live synchronized media.
* [1.2.4 Captions (Live) (AA) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/captions-live)
* Provide captions for live audio and video.
* [1.4.2 Audio Control (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/audio-control)
* Do not have audio that plays automatically on the page. When providing audio, also provide an easy way to disable the audio and adjust the volume.

# Video
* For pre-recorded video (without audio), provided a text alternative or audio descriptions that provide the same information presented 
* [1.2.3 Audio Description or Media Alternative (Prerecorded) (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/audio-description-or-media-alternative-prerecorded)
* For non-live video, provide a descriptive transcript or an audio description.
* [1.2.4 Captions (Live) (AA) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/captions-live)
* Provide captions for live audio and video.
[1.2.5 Audio Description (Prerecorded) (AA) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/audio-description-prerecorded)
* Videos should include “radio style” narration so that content makes sense if someone is consuming just the audio track. Include any text elements in the narration.

# Errors
[3.3.1 Error Identification (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/error-identification)
* Identify errors using aria-invalid.
* Make errors easy to discover, identify, and correct. 
* [3.3.3 Error Suggestion (AA) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/error-suggestion)
* If an input error is detected and if suggestions for correction are known, provide suggestions for fixing the submission.
* [3.3.4 Error Prevention (Legal, Financial, Data) (AA) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/error-prevention-legal-financial-data)

## Error Prevention
* Provide easy ways to confirm, correct, or reverse a user action where a mistake would cause a serious real-world consequence (e.g. submitting financial data, entering into a legal agreement, submitting test data, or making a transaction). 


# Hover and Focus
## Do’s
* For content that appears on hover and focus: the content should be dismissible with the escape key; the content itself can be hovered over; and the content remains available unless it is dismissed, it is no longer relevant, or the user removes hover and focus.
* To the extent possible, content that appears on hover or focus should not obscure other content, unless it presents a form input error. or can be dismissed with the escape key.

## Don’ts
* In general, avoid using scripts to remove focus from an element until the user moves focus manually.
* Avoid relying exclusively on pointer-driven events, such as onmouseover, to provide functionality when scripting. Generally, such functionality will also require scripting for keyboard operability.

# Tooltips
[1.4.13 Content on Hover or Focus (AA) (2.1) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/content-on-hover-or-focus)
* For tooltips, follow corresponding ARIA authoring practice.

# Tables
* Reserve tables for tabular data, use table headers appropriately, and use table captions.

# Frames
* Frames and iframes have descriptive titles.

# Status Messages
[4.1.3 Status Messages (AA) (2.1) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/status-messages)
* When conveying a status message, use ARIA live regions or ARIA alerts to announce the message to screen reader users.

# Languages
[3.1.1 Language of Page (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/language-of-page)
* Provide a lang attribute on the page’s html element.
[3.1.2 Language of Parts (AA) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/language-of-parts)
* If a portion of the page is in a different language, use the lang attribute on that part.

# Custom Widgets
* When creating a custom interactive widget, consult the ARIA Authoring Practices Document. Use ARIA labels, descriptions, roles, states, and properties to expose information about the component.

# Pointer Cancellation
* If a function is triggered on an up-event (e.g. onmouseup), provide a way to abort or undo the function.

# Keyboard Shortcuts
## Do’s
* [2.1.4 Character Key Shortcuts (A) (2.1) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/character-key-shortcuts)
* If a keyboard shortcut uses only letter (including upper- and lower-case letters), punctuation, number, or symbol characters, then the user must be able to disable the shortcut, remap the shortcut, or limit the shortcut to only when a particular interactive element has focus.

## Don’ts
[2.1.1 Keyboard (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/keyboard)
* Avoid implementing access keys. When access keys and other keyboard shortcuts are implemented, they must not interfere with existing browser and screen reader provided shortcuts.


# Other Don’ts

## Time Limits
[2.2.1 Timing Adjustable (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/timing-adjustable)
* Do not require time limits to complete tasks unless absolutely necessary. If a time limit is necessary, the time limit should be at least 20 hours, or it can be extended, adjusted, or disabled.

## Automatically moving content
[2.2.2 Pause, Stop, Hide (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/pause-stop-hide)
* Items on the page should not automatically move, blink, scroll, or update, including carousels. If content does automatically move, blink, scroll, or update, provide a way to pause, stop, or hide the moving, blinking, scrolling, or updating.

## Flashing content
[2.3.1 Three Flashes or Below Threshold (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/three-flashes-or-below-threshold)
* Do not provide any content that flashes more than three times in any 1-second period.

## Pointer Gestures
[2.5.1 Pointer Gestures (A) (2.1) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/pointer-gestures)
* Do not require multipoint or path-based gestures (e.g. pinching, swiping, dragging) for functionality unless the gesture is essential to the functionality. 

## Pointer Cancellation
[2.5.2 Pointer Cancellation (A) (2.1) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/pointer-cancellation)
* Avoid triggering functionality on down-events, such as onmousedown. Use events such as onclick instead.

## Motion Causing Changes
[2.5.4 Motion Actuation (A) (2.1) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/motion-actuation)
* Avoid activating functionality through motion (e.g. shaking a phone). If motion triggers functionality, provide a way to disable the motion trigger, and provide an alternative way to activate the functionality.

## Focus Causing Changes
[3.2.1 On Focus (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/on-focus)
* When the focus change, the page should not cause a change in page content, spawn a new browser window, submit a form, case further change in focus, or cause any other change that disorients the user.

## Inputs Causing Changes
[3.2.2 On Input (A) (2.0) (link is external)](https://www.w3.org/WAI/WCAG21/Understanding/on-input)
* When a user inputs information or interacts with a control, the page should not cause a change in page content, spawn a new browser window, submit a form, case further change in focus, or cause any other change that disorients the user. If an input causes such a change, the user must be informed ahead of time.

## Custom Widgets
* Avoid creating custom widgets when HTML elements already exist. For example, use a and button tags appropriately.


