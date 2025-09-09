## Font Size Guidelines

### Optimal font sizes for desktop

There are no exact rules for font sizing, but there are some generally good practices to think about when designing for desktop:

- **Body text** - Font sizes should be around `16px` to `18px` for legibility (or `1.6rem` to `1.8rem` using our sizing rules mentioned above). Keep in mind that more expressive typefaces may be less legible, so if you can afford to go a bit larger, then, even `21px` can be pleasant to read.
- **Headings** - The headings should be around `1.96` times larger than your body text to create a sufficient contrast. This would mean that if you use `18px` for body font size, then you would use around `35px` for headings. Expressive or experimental type type generally works best here, since the larger size makes it more legible.
- **Subheadings** - These should be slightly smaller than heading size, with some adjustments like less weight to create a contrast between the two. For example, if we used `35px` for the heading, we should use around `30px` for the subheading.
- **Input fields** - These should closely match the body text’s rules.

### Optimal font sizes for mobile

On mobile, you have less room to display your content. Additionally, users typically hold the devices closer to their eyes than they would a laptop or desktop screen - which means your typefaces can (and should) be smaller than on desktop:

- **Body text** - Font sizes should be at least `16px` for body text. In some cases, you may be able to go smaller (for example. if a typeface has unusually large characters or you are using uppercase letters), with 14px being the smallest you should go. For context, Google’s Material Design uses a minimum suggestion of `14px` for their secondary font size, while Apple’s guidelines use `15px` for theirs.
- **Headings** - Headings should be around `1.3` times larger than your body text to create a sufficient contrast. This would mean if you use `16px` for body font size, then you would use `~21px`. This is scaled down from the sizes we used on desktop.
- **Subheadings** - Here too, these would often be scaled down from the heading size, but we have a slight issue here in which the subheading may look too similar to the body font size. For this reason, some designers choose to make the subheading visually different through the use of weight, formatting like italics and letter spacing. If we used `21px` for a heading, we might choose `18px` or `16px` for a subheading, but with lighter weight than the heading or body text.
- **Input fields** - These should closely match the body text’s rules.

### Line heights

Line heights should increase as the width decreases, which does sound counter-intuitive. With a `base line-height: 1.5` it will only change by ±0.065 between 320px (20rem @ 16px) and 544px (34em @ 16px) so, unless you're a perfectionist, it could be ignored.

### Font units

When setting a font size I mostly use the rem unit, which references the pages root font-size, and eliminates cascade issues. Though, in the rare case where I'm relying on the cascade, I fallback to em. Kathleen McMahon has an in-depth piece covering why we should use relative units in CSS when setting type. [Pixels vs. Relative Units in CSS: why it’s still a big deal](https://www.24a11y.com/2019/pixels-vs-relative-units-in-css-why-its-still-a-big-deal/).

### Use fewer web fonts

The fastest font to deliver is a font that isn't requested in the first place. System fonts and variable fonts are two ways to potentially reduce the number of web fonts used on your site.

A system font is the default font used by the user interface of a user's device. System fonts typically vary by operating system and version. Because the font is already installed, the font does not need to be downloaded. System fonts can work particularly well for body text.

To use the system font in your CSS, list system-ui as the font-family:

```
font-family: system-ui
```

### Create Baseline Styles

It’s always good practice to reduce the guessing game that browsers play when they can’t find a style rule for a particular element.

Don’t forget to style basic HTML elements.

```
h1, h2, h3, h4, h5, h6 {  }
p { }
ol, ul { }
a { }
blockquote { }
pre, code { }
small { }
```

### Use Shorthand CSS

Always use shorthand wherever you can as it’s the conventional way of writing CSS nowadays.

- Here is the shorthand structure for the font property:
```
font: [font-style] [font-size]/[line-height] [font-family 1, font-family 2, ..., font-family n]
```
- For example:
```
p { font: normal 12px/1.5em Arial, Helvetica, sans-serif; }
```

## Font Size CSS Units

Default considered as a `96dpi` viewport with

```
:root {font-size:16px}
```

| POINT | PIXEL | EM/REM | PERCENT | KEYWORD |
|-------|-------|-------|-------|-------|
| `6pt` | `8px` | `0.5em` | `50%` |  |
| `6.75pt` | `9px` | `0.5625em` | `56.25%` | `xx-small` |
| `7pt` | `9.333px` | `0.5833em` | `58.33%` |  |
| `7.5pt` | `10px` | `0.625em` | `62.50%` | `x-small` |
| `8pt` | `10.667px` | `0.6667em` | `66.67%` |  |
| `8.25pt` | `11px` | `0.6875em` | `68.75%` |  |
| `9pt` | `12px` | `0.75em` | `75%` |  |
| `9.75pt` | `13px` | `0.8125em` | `81.25%` |  |
| `10pt` | `13.333px` | `0.8333em` | `83.33%` | `small` |
| `10.5pt` | `14px` | `0.875em` | `87.50%` |  |
| `11pt` | `14.667px` | `0.9167em` | `91.67%` |  |
| `11.25pt` | `15px` | `0.9375em` | `93.75%` |  |
| `12pt` | `16px` | `1em` | `100%` | `medium` |
| `12.75pt` | `17px` | `1.0625em` | `106.25%` |  |
| `13pt` | `17.333px` | `1.0833em` | `108.33%` |  |
| `13.5pt` | `18px` | `1.125em` | `112.50%` | `large` |
| `14pt` | `18.667px` | `1.1667em` | `116.67%` |  |
| `14.25pt` | `19px` | `1.1875em` | `118.75%` |  |
| `15pt` | `20px` | `1.25em` | `125%` |  |
| `15.75pt` | `21px` | `1.3125em` | `131.25%` |  |
| `16pt` | `21.333px` | `1.3333em` | `133.33%` |  |
| `16.5pt` | `22px` | `1.375em` | `137.50%` |  |
| `17pt` | `22.667px` | `1.4167em` | `141.67%` |  |
| `17.25pt` | `23px` | `1.4375em` | `143.75%` |  |
| `18pt` | `24px` | `1.5em` | `150%` | `x-large` |
| `18.75pt` | `25px` | `1.5625em` | `156.25%` |  |
| `19pt` | `25.333px` | `1.5833em` | `158.33%` |  |
| `19.5pt` | `26px` | `1.625em` | `162.50%` |  |
| `20pt` | `26.667px` | `1.6667em` | `166.67%` |  |
| `20.25pt` | `27px` | `1.6875em` | `168.75%` |  |
| `21pt` | `28px` | `1.75em` | `175%` |  |
| `21.75pt` | `29px` | `1.8125em` | `181.25%` |  |
| `22pt` | `29.333px` | `1.8333em` | `183.33%` |  |
| `22.5pt` | `30px` | `1.875em` | `187.50%` |  |
| `23pt` | `30.667px` | `1.9167em` | `191.67%` |  |
| `23.25pt` | `31px` | `1.9375em` | `193.75%` |  |
| `24pt` | `32px` | `2em` | `200%` | `xx-large` |
| `24.75pt` | `33px` | `2.0625em` | `206.25%` |  |
| `25pt` | `33.333px` | `2.0833em` | `208.33%` |  |
| `25.5pt` | `34px` | `2.125em` | `212.50%` |  |
| `26pt` | `34.667px` | `2.1667em` | `216.67%` |  |
| `26.25pt` | `35px` | `2.1875em` | `218.75%` |  |
| `27pt` | `36px` | `2.25em` | `225%` |  |
| `27.75pt` | `37px` | `2.3125em` | `231.25%` |  |
| `28pt` | `37.333px` | `2.3333em` | `233.33%` |  |
| `28.5pt` | `38px` | `2.375em` | `237.50%` |  |
| `29pt` | `38.667px` | `2.4167em` | `241.67%` |  |
| `29.25pt` | `39px` | `2.4375em` | `243.75%` |  |
| `30pt` | `40px` | `2.5em` | `250%` |  |
| `30.75pt` | `41px` | `2.5625em` | `256.25%` |  |
| `31pt` | `41.333px` | `2.5833em` | `258.33%` |  |
| `31.5pt` | `42px` | `2.625em` | `262.50%` |  |
| `32pt` | `42.667px` | `2.6667em` | `266.67%` |  |
| `32.25pt` | `43px` | `2.6875em` | `268.75%` |  |
| `33pt` | `44px` | `2.75em` | `275%` |  |
| `33.75pt` | `45px` | `2.8125em` | `281.25%` |  |
| `34pt` | `45.333px` | `2.8333em` | `283.33%` |  |
| `34.5pt` | `46px` | `2.875em` | `287.50%` |  |
| `35pt` | `46.667px` | `2.9167em` | `291.67%` |  |
| `35.25pt` | `47px` | `2.9375em` | `293.75%` |  |
| `36pt` | `48px` | `3em` | `300%` |  |


## Reference

- [The Responsive Website Font Size Guidelines](https://www.learnui.design/blog/mobile-desktop-website-font-size-guidelines.html)
- [Pixels are dead](https://medium.com/@julienetienne_/pixels-are-dead-faa87cd8c8b9)
- [CSS units for font-size: px | em | rem](https://medium.com/@dixita0607/css-units-for-font-size-px-em-rem-79f7e592bb97)
