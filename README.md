# SASS intro / basic

## Install:

npm install -g sass

About:
Syntactically Awesome Style Sheets
Sass is a stylesheet language that’s compiled to CSS. It allows you to use variables, nested rules, mixins, functions, and more, all with a fully CSS-compatible syntax. Sass helps keep large stylesheets well-organized and makes it easy to share designs within and across projects.
….Source link
Access pseudo without one more write same class:
.btn {
&:hover { }
&:hover{ }
&:active{ }
}

Lighten & darken:
background-color: darken($color: $bgColor, $amount: 5%);
background-color: lighten($color: $bgColor, $amount: 5%);

@mixin and @include:

Example -1:
@mixin reset {
margin: 0;
padding: 0;
box-sizing: border-box;
}
Use:
body {
@include reset;
}
Example -2:
@mixin box($bgColor) {
margin-bottom: $boxMarginBottom;
height: $boxHeight;
width: $boxWidth;
background: $bgColor;
color: $boxTextColor;
}
Use:
.box-1 {
@include box(green);
}
.box-2 {
@include box(yellow);
}

Describe:
@mixin and @include are like inheritance.

@mixin and @include with if else (light and dark theme)
@mixin theme-colors($theme) {
@if $theme == "light" {
background-color: $light-bg;
} @else {
background-color: $dark-bg;
}
}

@each:
@each $var in lists

$sizes: 40px, 50px, 80px;
@each $size in sizes {
    .icon-#{$size}{
font-size: $size;
}
}

Function: …comming soon
