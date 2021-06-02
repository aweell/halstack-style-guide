# Date-picker

A date input is a user interface element where the user can type or select a date in a predefined format. The date format depends on an ISO definition for each country and the preference of use within the application.

The format of the date may vary depending on language, region, country or customer. i.e.

- The default format for the United States is mm/dd/yyyy
- The default format for Australia, Europe, Africa, So America and much of Asia is dd/mm/yyyy
- The default format in China is yyyy/mm/dd

It is a good practice to give to the user some type of hint about the date format and in many cases, there is a second way to select the date with a date picker control.
In this component both options will be available to the user, so if the user gets stuck typing the correct format of the data it has an additional option with graphic representation that is easily used.

It is common to find a date picker in these scenarios: date of birth, date range or as an input to filter based on some criteria.

If the state of the input is empty, it should give a hint in the placeholder about the format required. Also, as the design system is based in some of the Angular Material guidelines, that format would be visible in case that the input component is selected or filled.

## Appereance

The date input should lead the user to interact with it to select a date and give appropiate feedback to the user to know what value is selected from the wide range. It should be intuitive, navigable and useful.

### Modes

There is only one mode to represent the date that follows the design of the rest inputs. A thin line under the input container with description and labeling, and some animations that activate when the user interacts with the component.
Modes: **basic**.

![Date modes](images/date_modes.png)

### States

Six different states are defined in the life cycle of the component: **normal**, **disabled**, **entered**, **selected**, **focused** and **datepicker focused**.

![Date states](images/date_states.png)

### Calendar Pop-up

The calendar pop-up displays the different views of days, months and years.
By default, the view of the calendar will be the current month with all of its days and it will appear right below the input.

The user can navigate through the calendar to select the desire date.

![Views of the datepicker](images/date_datepicker.png)

### Design Interactions

Different feedback and outcomes happen when the calendar pop-up is used. To see more information please, open the xd file linked with the date component in this respository.

## Design tokens

| Tokens                            | Default value |
| --------------------------------- | ------------: |
| pickerSelectedDateBackgroundColor |     `#6F2C91` |
| pickerSelectedDateColor           |     `#FFFFFF` |
| pickerBackgroundColor             |     `#FFFFFF` |
| pickerFontColor                   |     `#000000` |
| pickerActualDate                  |     `#D9D9D9` |
| pickerHoverDateBackgroundColor    |     `#D0BDDB` |
| pickerHoverDateFontColor          |     `#000000` |
| scrollBarThumbColor               |     `#666666` |
| scrollBarTrackColor               |     `#D9D9D9` |
| focusColor                        |     `#005FCC` |

The other attributes of the date component are inherited from the input component because it is used internally in the date implementation, so a change in any token of the text field component will affect this component too.

### Design Specifications

![date-picker specifications](images/date_specs.png)

The specifications for dates are similar to the ones used with the input text component. In the case that the field will be read-only, the look and feel will be the same for both components.

The text within the input should always aligns left. By default, the font size for this type of component is 16 pixels. When the field is empty and it has some hint the space between the text and the line below the input should be 7 pixels.

In the case that the input is selected or the user is typing inside and the hint is positioned on the top, the measures are 7 pixels between the main text and the underline decoration and 6 pixels between the top hint respect the main text. As this will take more space, the height of the component will be changed from 32 pixels to 48 pixels. Another variation could be to having an auxiliary text below the underlined item so it will take 73 pixels for the height.

The font for the label at the top and the auxiliary text must be 12 pixels.

The thickness of the border should be 1 pixel but in case that the input will be selected, the width would change to 2 pixels with animation between the two states inherit from Angular Material default behavior.

Smaller touch points decrease the ease of use of the interface because it is costly for the user to hit the target. To prevent that, the size defined for the date picker icon is 20 pixels by 20 pixels for the desktop version and 44 pixels by 44 pixels for mobile and tablet versions of the application.
These sizes are including small padding as a touchable safe area so the size of the icon in both cases will be 2 pixels less in wide and tall.

#### Height

| Property                            |       Value |
| ----------------------------------- | ----------: |
| Height (default)                    |      `32px` |
| Height (selected)                   |      `48px` |
| Height (selected + auxiliar text)   |      `73px` |


#### Width

| Property         |  value            | 
| :---                |     :---             |   
| `medium`_(default)_    |  240px           | 
| `large`          |  480px           |  
| `fillParent`    |  -                   | 


#### Margin

Different values can be applied to each side of the component:
```top``` ```bottom``` ```left``` ```right```

margin | Value
-- | --
`xxsmall` | 6px
`xsmall` | 16px
`small` | 24px
`medium` | 36px
`large` | 48px
`xlarge` | 64px
`xxlarge` | 100px


#### Typography

| Property                            |       Value |
| ----------------------------------- | ----------: |
| Font size default                   |      `16px` |
| Font size label                     |      `12px` |
| Font size placeholder               |      `16px` |
| Font size assistive text/error message                     |      `12px` |
| Font weight                         |   `Regular` |

#### Other specs

| Property                            |       Value |
| ----------------------------------- | ----------: |
| Border thickness                    |   `1px/2px` |
| Icon size                           | `20x20(px)` |
| Distance between text and underline |       `7px` |

### Additional modes

For the datepicker as for the input component are additional modes apart from the normal ones. **Required**, **error** and **assistive text** are another options to display within the component.

The different modes and states can be combined between them to handle the flow of the component.

![Additonal modes for datepicker](images/date_additionals.png)

### Calendar Pop-up Specifications

The majority of the specifications are the same as in Angular Material datepicker component. In the table below is pointed all the relevant information.

| Property         |       Value |
| ---------------- | ----------: |
| Padding          |      `20px` |
| Height (default) |     `354px` |
| Widht (default)  |     `296px` |
| Circle size      | `28x28(px)` |
| Circle thickness |       `1px` |
| Font weight      |   `Regular` |
| Font size        |      `13px` |

![Date specifications for picker](images/date_picker_specs.png)

## Links and references

- https://xd.adobe.com/view/23e2cca4-5021-490a-a548-e99a9b4a2006-76b1/screen/7965bd24-3ef3-427d-92de-0d2aac880402/variables/
