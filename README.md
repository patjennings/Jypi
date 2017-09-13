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
    <div class="row">
      ...
    </div>
Then define your spaces and span - if you declared a 8 columns system
    <div class="row">
      <div class="col-4 span-2">
        ...
      </div>
    </div>

## Typography
Declared for reading comfort from desktop to mobile devices

## Components
### Buttons
delivered with various classes
### Forms
Declare forms in

## Add custom fonts
Add custom Base64 CSS font files
