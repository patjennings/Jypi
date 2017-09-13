# styles-sandbox
A starting set for websites & various applications.

## Installation
    $ npm install

## Start
    $ cd /styles-sandbox
    $ npm start
This will run the gulp task that compile sass files, fonts, js & images

work in `/client`, then Gulp compiles in `/public`

## Configuration
### Variables
In \_variables.scss file
BaseRem is used to ensure visual consistency across the styles
### Mixins
Use for transition handled for all browsers

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
Declared for reading comfort from desktop to mobile devices. Print is especially improved for A4 input size.

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
Add custom Base64 CSS font files
