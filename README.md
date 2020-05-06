# x-ui

x-ui is based on a modified/stripped version of [Tachyons CSS](http://tachyons.io/), a functional CSS framework.

Some of the original utility classes have been removed, and others have been added, along with a reorganization of the available breakpoints, support for custom color palettes, and minimal browser reset styles. 

__These are an opinionated choice and built for my personal use__, but it is still very flexible to add/change almost everything and still keep the same Tachyons like API concept intact.

## Quick usage

If you would like to give it a spin, using the default color scheme and settings provided, place this in the `<head>` of your HTML file:
```
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/syndicatefx/x-ui/x-ui.min.css">
```

### Example components

A work-in-progress list of examples you can copy/paste and modify can be found on this [Codepen collection](https://codepen.io/collection/nmpOPG)

## What utilities have been removed from the original

- normalize.css
- font families
- skins and skins:pseudo
- border colors
- box-shadows
- floats, clears and clearfix
- table styling classes
- debug classes
- show/hide class hover classes
- add box-shadow on hover classes
- breakpoint *-ns
- all `.aspect-ratio-*` classes
- transitions from `.link` class
- `.dim`, `.glow` and `.underline-hover`
- `.bg-animate`, `.grow` and `.grow-large`

## What has been Modified/added

- A separate `vars.sass` file to edit/modify color variables, breakpoint values and transition timing and duration
- Minimal reset and basic browser default overrides
- Default system fonts only
- Opinionated color palette for background-color, border-color and color.
- The above color palette also contemplates :hover & :focus states for background-color, border-color and color
- Custom box-shadow utility classes
- breakpoints use min-width only
- new default breakpoints:

    - `*-m` = 640px
    - `*-l` = 960px
    - `*-xl` = 1280px

- `.hover-animate` (with editable timing and easing variables in vars.sass), which when used together with `.hover-*` classes adds transition animation to all background-color, border-color, color
- `.mt-auto` and `.mb-auto` classes

### Forms

The `_forms.sass` file includes a hard reset for all form elements and some default styles and classes for checkbox and radio inputs. This is an experiment on building custom designed form elements using as much of the available utility classes as possible. The pros are that you can design everything in your markup without touching the css, the cons are that it will require more markup to achieve the desired effect. Use at your own risk, or delete and substitute these with something more robust like [formbase.css](https://github.com/electerious/formbase)