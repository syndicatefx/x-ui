# x-ui

x-ui is based on a modified/stripped version of [Tachyons CSS](http://tachyons.io/), a functional CSS framework.

Some of the original utility classes have been removed, and others have been added, along with a reorganization of the available breakpoints, support for custom color palettes, box-shadows, and minimal browser reset styles. 

__These are an opinionated choice and built for my personal use__, but still very flexible to add/change almost everything to suit specific use cases.

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

- A separate `vars.sass` file to edit/modify deafults for: typescale, spacing(applied to paddings, margins, fixed widths and heights), color list, box-shadow list, breakpoint values, transition timing and duration
- Minimal reset and basic browser default overrides
- Default system fonts only
- Basic color palette for wireframing (background-color, border-color and color)
- The above color palette also contemplates :hover & :focus states for background-color, border-color and color
- Custom box-shadow utility classes, includes :hover & :focus states for each
- breakpoints use min-width only
- new default breakpoints:

    - `*-m` = 640px
    - `*-l` = 960px
    - `*-xl` = 1280px

- `.hover-animate` (with editable timing and easing variables in vars.sass), which when used together with `.hover-*` classes adds transition animation to all background-color, border-color, color and box-shadows
- `.mt-auto` and `.mb-auto` classes
- `.z-*`, `.o-*` now available in all breakpoints, and a new `.z--1`: `z-index: -1` was added to all breakpoints too.

### Forms

The `_forms.sass` file includes some default properties for inputs. This is an experiment on building custom designed form elements using as much of the available utility classes as possible. The pros are that you can design almost everything in your markup without touching the css, the cons are that it will require more markup to achieve the desired effect. Use at your own risk, or delete and substitute these with something more robust like [formbase.css](https://github.com/electerious/formbase)

#### Example

Using _forms.sass you can customize checkbox, radio and select this way:

Radio buttons:

```html
    <div class="mv4">
        <label class="db f6 fw7 mb3 color-3">Choose a finish</label>
        <label class="relative flex items-center mb3 color-3">
            <input class="clip" type="radio" name="finish" checked="">
            <span class="db w1 h1 mr2 ba b--color-2 br-100" aria-hidden="true"></span>
            <svg viewPort="0 0 8 8" width="8" height="8" fill="currentColor" class="absolute ml1" aria-hidden="true">
                <circle cx="4" cy="4" r="4"/>
            </svg>
            Mate
        </label>
        <label class="relative flex items-center mb3 color-3">
            <input class="clip" type="radio" name="finish">
            <span class="db w1 h1 mr2 ba b--color-2 br-100" aria-hidden="true"></span>
            <svg viewPort="0 0 8 8" width="8" height="8" fill="currentColor" class="absolute ml1" aria-hidden="true">
                <circle cx="4" cy="4" r="4"/>
            </svg>
            Gloss
        </label>
    </div>
```

Checkbox:

```html
    <label class="relative flex items-center mb3 color-3">
        <input class="clip" type="checkbox" checked="">
        <span class="db w1 h1 mr2 ba b--color-2 br2" aria-hidden="true"></span>
        <svg viewPort="0 0 16 16" width="16" height="16" class="absolute" aria-hidden="true">
            <polyline points="3,8 7,12 13,4" fill="none" stroke="currentColor" stroke-width="2"/>
        </svg>
        Send me updates
    </label>
```

Select:

```html
    <label class="db f6 fw7 mb3 color-3" for="country">Choose materials</label>
    <div class="relative mb4">
        <select class="input-reset w-100 pa2 mb3 color-3 bg-color-0 ba b--color-2 hover-animate hover-b--color-3 br2" id="country">
            <option value="china">Plastic</option>
            <option value="russia">Metal</option>
            <option value="usa" selected="">Wood</option>
        </select>
        <svg viewPort="0 0 16 12" width="16" height="12" fill="none" stroke="currentColor" stroke-width="2" class="absolute right-0 top-1 mr2 nt1 color-3" aria-hidden="true">
            <polyline points="2,2 8,8 14,2" />
        </svg>
    </div>
```
