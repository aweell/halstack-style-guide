## Overview

Text inputs are input fields typically used in forms that allow the user to enter text data in a structured format.

## Usage

Use text inputs in forms to help people enter, select, and search for text. They can also be part of a modal, search, etc...

Common text input types include: 
* Usernames
* Descriptions
* URLs
* Phone numbers
* Credit cards
* Emails, addresses
* Plain text searches

### Do's

* Do use fixed width inputs for content that has a specific, known length (e.g. post code, phone number).
* Do use sentence for any input text case with standard, local grammar and punctuation rules.
* Do use helpful and clear text for labels, error messages and helper texts


### Dont's

* Do not use text-input for text longer than a single line (e.g. name, phone number). Use the text-area instead.
* Do not disable copy and paste.
* Do not display pop up error message after validating
* Avoid masking label, keep it always visible.


## Appearance

The input appearance must be simple and clear, in this design system text inputs are represented as a placeholder with a thin underline where the text will be written.
Other elements like assistive text, prefix or suffix icons or error handlers can be complementing the input field making the basic structure more informative.

### Modes

Four different modes can be identify using text input component: **default**, **default with preffix**, **default with suffix** and **default with preffix and suffix**.

![Input modes example](images/input_modes.png)

### States

The states for text input are: **normal**, **focused**, **invalid** and **disabled**.

![Input states example](images/input_states.png)

### Placement and alignment

Where possible, ensure that field lengths provide meaningful affordances that help people answer questions effectively. Otherwise, utilize a consistent length that provides enough room for correct answers.

## Design tokens

| Tokens                        | Default value |
| ----------------------------- | ------------: |
| fontColor                     |     `#000000` |
| disabledFontColor             |     `#B1B1B1` |
| error                         |     `#D0011B` |
| selectedOptionBackgroundColor |     `#F2F2F2` |
| hoverOptionColor              |     `#000000` |
| scrollBarThumbColor           |     `#666666` |
| scrollBarTrackColor           |     `#D9D9D9` |

## Text Area

The text area is a variation inside the text input component. The functionality of both components is the same, the user can enter text in the input area that later will be processed by the application. However, the text area is made to match with a large data text, like a description, paragraph, a long address or a comment.
When the amount of information given by the user needs to be precise and detailed, the application should use this element for that purpose.

It allows multiple lines, adapting the text to the space available and in the case that there won't be enough space then the text will be overlapped and a scrollbar will be used to scroll up and down to see the rest of the information. 

The text area can have the following features: Label, assistive text and scrollbar.

The aspects that text area is not including respecting text input are:

- Prefix and suffix
- Max height fixed

![Textarea example](images/input_textarea.png)

## Design Specifications

### Width

width | value
-- | --
```small``` | 60px
```medium``` (_default_) | 240px
```large``` | 480px
```fitContent``` | -
```fillParent``` | -

## Height

| Property                                       |       Value |
| ---------------------------------------------- | ---------- |
| `min-height`                                   |      32px |
| `max-height`                                   |      73px |

### Margin

margin | value
-- | --
```xxsmall``` | 6px
```xsmall``` | 16px
```small``` | 24px
```medium``` | 36px
```large``` | 48px
```xlarge``` | 64px
```xxlarge``` | 100px

And also apply different values to each side of the component:
```top``` ```bottom``` ```left``` ```right```

### Typography

| Property                                       |     Value |
| ---------------------------------------------- | --------- |
| `font-size` (_default_)                        |      16px |
| `font-size` (_label_)                          |      12px |
| `font-weight`                                  |   Regular |

### Spacing

| Property                                       |     Value |
| ---------------------------------------------- | --------- |
| Input value `padding-top`                      |      6px |
| Input value `padding-bottom`                   |      7px |
| Distance between preffix and value             |     12px |
| Distance between suffix and value              |     12px |

### Other

| Property                                       |       Value |
| ---------------------------------------------- | ----------: |
| Border thickness                               |     1px/2px |
| Icon size                                      |   20x20(px) |


![Specifications for input component](images/input_specs.png)

### Optional/mandatory fields

Required fields are a variation in the normal behavior of the input fields. This indicates to the user that the input is required so it can't be skipped if the intention is to go forward in the application.


* Try to avoid optional input fields in forms.
* If most of the inputs on a form are required, indicate the few that are optional.
* If most of the inputs on a form are optional, indicate the few that are required.
* When indicating what form fields are either required or optional, text is the most clear. However, the * symbol is relatively well understood to mean required.
If you do use * to indicate required fields, don’t forget a legend that explains what it indicates.



Here are the different representations of a required field:

![Type required in input texts](images/input_required.png)

The specifications for the required input follows the same guide that a normal input, with the variation of the asterisk before the label.

### Helper text

Helper text can be used as additional instructions to the user when filling in the form. It should be visible even on focus state and it can be replaced by an error message until the error is fixed in order to prevent adding more lines of text.

**Usage**

Do:

* Keep helper text as short and specific as possible.
* Only use helper text when truly necessary to avoid overloading the user.
* Should give an example or an explanation of the field

Don’t:

* Helper text should not run longer than the input area.

**Specs**

| Property | Element | Token | Value |
| :---         |     :---     |          :--- |         :--- |
| `margin-top`  | `input-helper-text`    |     | 6px 
| `font-size`  | `input-helper-text`    |  `type-scale-01`   | 12px 
| `font-family`  | `input-helper-text`    |  `type-sans`   | Open Sans 
| `color` | `input-helper-text`      |  `Hal-Black`   |  hsl(0, 0%, 0%) |

### User Interface Design Considerations

- Input fields should allow users to enter any combination of letters, numbers, or symbols unless otherwise restricted or stipulated by requirements
- Avoid breaking up a number with distinct sections into separate input field (i.e. phone numbers, area codes, SSN, dates, etc) to facilitate screen reader accessibility requirements
- Allow sufficient space in an entry field to allow typical input
- User text areas, rather than a single-line input box for paragraph text and comments
- Input fields are more restrictive for mobile users to make sure the type of input field is warranted
- Only show error validation messages after the user has left the field

## Links and references

- https://xd.adobe.com/view/23e2cca4-5021-490a-a548-e99a9b4a2006-76b1/screen/1cad53d5-9b24-4336-a0c9-3d4b283c9088/variables/

