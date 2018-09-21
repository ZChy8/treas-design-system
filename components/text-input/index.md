---
layout: page
parent: "Components"
title: "Text Input"
intro: "Text input fields allow people to enter any combination of letters, numbers, or symbols of their choosing (unless otherwise restricted)."
jump_menu: true
---

<div class="ds-preview">
  <p><input class="treas-input" type="text" name="some_name2" placeholder="Placeholder" value="Text"></p>
</div>

## Variations

The style for `<input>` text components always start with `class="treas-input"`, modifiable with one or multiple `treas-input--[variation]`.

```html
<input class="treas-input treas-input--[variation]" type="text" name="some_name" value="">
```

### Default

```html
<p><input class="treas-input" type="text" name="1iuoytytesgdf" value="Text" placeholder="Placeholder"></p>
```
<div class="ds-preview">
  <p><input class="treas-input" type="text" name="1iuoytytesgdf" value="Text" placeholder="Placeholder"></p>
</div>

### Round

```html
<p><input class="treas-input treas-input--round" type="text" name="1idf" value="Text" placeholder="Placeholder"></p>
```
<div class="ds-preview">
  <p><input class="treas-input treas-input--round" type="text" name="1idf" value="Text" placeholder="Placeholder"></p>
</div>

### Full-width

```html
<p><input class="treas-input treas-input--block" type="text" name="155tj" value="Text" placeholder="Placeholder"></p>
```
<div class="ds-preview">
  <p><input class="treas-input treas-input--block" type="text" name="155tj" value="Text" placeholder="Placeholder"></p>
</div>

### Small

```html
<p><input class="treas-input treas-input--small" type="text" name="qwerty" value="Text" placeholder="Placeholder"></p>
```
<div class="ds-preview">
  <p><input class="treas-input treas-input--small" type="text" name="qwerty" value="Text" placeholder="Placeholder"></p>
</div>

### Large

```html
<p><input class="treas-input treas-input--large" type="text" name="ytrewq" value="Text" placeholder="Placeholder"></p>
```
<div class="ds-preview">
  <p><input class="treas-input treas-input--large" type="text" name="ytrewq" value="Text" placeholder="Placeholder"></p>
</div>

### Response: Error

```html
<p><input class="treas-input treas-input--error" type="text" name="7id" value="Text"></p>
```
<div class="ds-preview">
  <p><input class="treas-input treas-input--error" type="text" name="7id" value="Text"></p>
</div>

### Response: Success

```html
<p><input class="treas-input treas-input--success" type="text" name="lorem" value="Text"></p>
```
<div class="ds-preview">
  <p><input class="treas-input treas-input--success" type="text" name="lorem" value="Text"></p>
</div>

### Disabled

Disabled fields do not have a `class="treas-input--[variation]"`, instead using the `disabled` attribute.

```html
<p><input class="treas-input" disabled="disabled" type="text" name="1224hd9f" value="Text"></p>
```
<div class="ds-preview">
  <p><input class="treas-input" disabled="disabled" type="text" name="1224hd9f" value="Text"></p>
</div>

### Readonly

Readonly fields do not have a `class="treas-input--[variation]"`, instead using the `readonly` attribute.

```html
<p><input class="treas-input" readonly="readonly" type="text" name="4f" value="Text"></p>
```
<div class="ds-preview">
  <p><input class="treas-input" readonly="readonly" type="text" name="4f" value="Text"></p>
</div>

## Usage

### Use When

* If you can’t reasonably predict a user’s answer to a prompt and there might be wide variability in users’ answers.
* When using another type of input will make answering more difficult. For example, birthdays and other known dates are easier to type in than they are to select from a calendar picker.
* When users want to be able to paste in a response.
* When users need only a single line of entry.

### Don't Use

* When the value user enter are limited in amount
* When users are choosing from a specific set of options. Consider [select]({{ site.baseurl }}components/select/), [radio]({{ site.baseurl }}components/radio/), or [checkbox]({{ site.baseurl }}components/checkbox/).
* When users need to enter multiple lines of content, consider the [textarea]({{ site.baseurl }}components/textarea/) element.

## Accessibility

If you customize the text inputs, ensure they continue to meet the the accessibility requirements that apply to all form controls.

* Do not use the `placeholder` attribute as the sole label for accessibility reasons. Form components must have an associated `<label>` with matching `for` attribute. Additionally, most browsers’ default rendering of placeholder text does not provide a high enough contrast ratio to sufficiently serve as the sole label.
* Avoid breaking numbers with distinct sections (such as phone numbers, Social Security Numbers, or credit card numbers) into separate input fields. For example, use one input for phone number, not three (one for area code, one for local code, and one for number). Each field needs to be labeled for a screen reader and the labels for fields broken into segments are often not meaningful.

## General Guidance

* The length of the text input provides a hint to users as to how much text to write. Do not require users to write paragraphs of text into a single-line input box; use a [textarea]({{ site.baseurl }}components/textarea/) instead.
* Text inputs are among the easiest type of input for desktop users but are more difficult for mobile users.
* Consider the type of content a user may enter to aid mobile device entry; mobile devices typically surface a keyboard UI attuned to the type. For example, `type="tel"` will surface a [phone keyboard](http://html5doctor.com/html5-forms-input-types/#input-tel).
* Only show error validation messages or styling after a user has interacted with a particular field; avoid significantly updating styles while a user is actively entering input.
* Do not use the `placeholder` attribute in place of a `<label>` element. Its purposes is different: the standard `<label>` describes the role of the form element; that is, it indicates what kind of information is expected. The `placeholder` attribute is typically a hint about the format the content should take. There are cases in which the placeholder attribute is not displayed to the user (e.g. when input field has a value), so the form must be understandable without it.