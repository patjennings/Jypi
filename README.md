# Jypi
Jypi is a starter kit for designing websites & various applications.

## Installation
    $ npm install

## Start
    $ cd /Jypi
    $ npm start
This will run the gulp task that compile sass files, fonts, js & images

work in `/client`, then Gulp compiles in `/public`

## Configuration
You should include `_variables.scss` and `_mixins.scss` at the top of each new sass file like this:
```css
@import 'variables';
@import 'mixins';
```

### Variables
In `client/sass/_variables.scss`

These values will ensure visual consistency across your website. Every (every) spacing, font-size or whatever is based on this ($baseRem for screen, $basePt for print).
```scss
$baseRem: 1rem;
$basePt: 10.5pt;
```
The total width of your main container. It can be fixed, or floating (e.g.100%)
```scss
$totalWidth: 1366px;
```
The column-width of your grid in pixels — should be even like 6, 8, 12, 14, etc.
```scss
$columns: 8;
```
The gutter-width of your grid in pixels
```scss
$gutter: 32px;
```
The breakpoints for responsive behaviour. Basically : smartphone, portrait tablet & laptop++
```scss
$break-small: 640px;
$break-medium: 800px;
$break-large: 1170px;
```
The main values for standard animations. Help consistency across each small animation, like hovers
```scss
$hoverSpeed: 0.2s;
$hoverEase: ease-in-out;
```

### Mixins
Use mixin for cross-browser features
Simple transition
```scss
@include transition(all, 0.2s, ease-in-out);
```
For a keyframe-based animation, you can use this
```scss
// Declare animation like this
@include animation('myAnimation .5s cubic-bezier(0.5, 0, 0.5, 1)');
// Maybe you will want to delay start
@include animation-delay(2s);
// Here are the keyframes  
@include keyframes(myAnimation){
  0%{
    opacity: 0;
  }
  100%{
    opacity: 1;
  }
}
```
For border-radius
```scss
@include border-radius; // With the default value (4px)
@include border-radius(8px); // Or with a custom value
```

## Layout
Column-based layout
Declare in a row
```html
<div class="row">
  ...
</div>
```
Then define your spaces and span - if you declared a 8 columns system
```html
<div class="row">
  <div class="col-4 span-2">
    ...
  </div>
</div>
```

## Typography
This part is crafted for legibility and reading comfort from desktop to mobile devices. Print is especially improved for A4 output size.

## Components
### Buttons
Delivered with various classes
Default button
```html
<button class="btn" type="button">Label</button>
```
Then you can add validate, caution, big, small, and mix them.
```html
<button class="btn validate big" type="button">Label</button>
```
Or, you can say it has no borders
```html
<button class="btn no-stroke" type="button">Label</button>
```
### Forms
Declare forms like this
```html
<div class="form--wrapper">
  ...
</div>
```

```html
<div class="form--wrapper">
  <label for="emailAdress">Email address</label>
  <input type="email" class="form-control" id="emailAdress" placeholder="Email">
</div>
```

## Add custom fonts
Add custom Base64 CSS font files.

Original .woff files are stored in `client/fonts/`, named like this:

- `{type}-{weight}.woff`
- `{type}-{weight}-i.woff` for italic.

So, there will be files like `sans-400.woff` or `mono-700.woff` at the root of `client/fonts/`; then Gulp will process that and output everything in `client/sass/fonts.css`.

- `{type}` can be mono, serif or sans.
- `{weight}` can be everything from 100 (thin) to 900 (black).

This file is then imported and used in `client/sass/_variables.scss`, and you can call `'font-family: $serif'` or `'$sansSerif'` or `'$mono'` everywhere.
