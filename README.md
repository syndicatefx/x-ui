# x-ui

x-ui is based on a modified/stripped version of [Tachyons CSS](http://tachyons.io/), a functional CSS framework.

Some of the original utility classes have been removed, and others have been added, along with a reorganization of the available breakpoints, support for custom color palettes, box-shadows, and minimal browser reset styles. 

__This is an opinionated structure built for my personal use__, but still very flexible to add/change almost everything to suit specific use cases.

## Usage

Required nodejs and npm installed.

- Install: `$ npm install`
- Build: `$ npm build`
- Dev with watch & browsersync: `$ npm start`

Edit `theme.css` file to change variable settings for: typescale, spacing(applied to paddings, margins, fixed widths and heights), colors, box-shadows, transition timing and duration, breakpoint values.  

## What utilities have been removed from the original Tachyons

- 🚫 normalize.css
- 🚫 font families
- 🚫 skins and skins:pseudo
- 🚫 border colors
- 🚫 box-shadows
- 🚫 floats, clears and clearfix
- 🚫 table styling classes
- 🚫 debug classes
- 🚫 show/hide class hover classes
- 🚫 add box-shadow on hover classes
- 🚫 breakpoint `*-ns`
- 🚫 all `.aspect-ratio-*` classes
- 🚫 transitions from `.link` class
- 🚫 `.dim`, `.glow` and `.underline-hover`
- 🚫 `.bg-animate`, `.grow` and `.grow-large`

## What has been Modified/added

- Minimal reset and basic browser default overrides
- Default system fonts or if browser supports variable fonts, use the [PT Root UI](https://www.paratype.com/fonts/pt/pt-root-ui) typeface included
- Basic color palette for wireframing (for background-color, border-color and color)
- The above color palette also contemplates `:hover`, `:focus` and `:active` states for `background-color`, `border-color` and `color`
- Custom box-shadow utility classes, includes `:hover` & `:focus` states for each
- Basic form presets
- breakpoints use min-width only
- new default breakpoints:

    - `*-m` = 640px
    - `*-l` = 960px
    - `*-xl` = 1280px

- `.hover-animate` with editable timing and easing variables in `theme.css`, which when used together with `.hover-*`, `.focus-*`ad `.active-*` classes adds transition animation
- `.mt-auto` and `.mb-auto` classes
- `.z-*`, `.o-*` now available in all breakpoints, and a new `.z--1`: `z-index: -1` was added to all breakpoints too.