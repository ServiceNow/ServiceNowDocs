---
title: Service Portal SCSS Primer
description: SCSS is a subset of the Syntactically Awesome StyleSheets \(Sass\) specification and is an extension of CSS. Every valid CSS style sheet is valid SCSS.SCSS variables are a way to store information that you want to reuse throughout your style sheet. You can store things like colors, font stacks, or any CSS value you think you want to reuse. SCSS uses the $ symbol to make something a variable.List of functions for Service Portal SCSS compiler.SCSS lets you nest your CSS selectors in a way that follows the same visual hierarchy of your HTML.SCSS has a handful of standard math operators like +, -, \*, /, and %.A mixin lets you make groups of CSS declarations that you want to reuse throughout your site. You can pass in values to make your mixin more flexible.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Service Portal reference, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Service Portal SCSS Primer

SCSS is a subset of the Syntactically Awesome StyleSheets \(Sass\) specification and is an extension of CSS. Every valid CSS style sheet is valid SCSS.

**Parent Topic:**[Service Portal reference](reference-service-portal.md)

## SCSS variables

SCSS variables are a way to store information that you want to reuse throughout your style sheet. You can store things like colors, font stacks, or any CSS value you think you want to reuse. SCSS uses the $ symbol to make something a variable.

SCSS supports the follow data types:

-   Numbers \(including units\)
-   Strings \(with quotes or without\)
-   Colors \(name, or names\)
-   Booleans

Variables can also be arguments to or results from one of several available functions or mixins. During translation, the values of the variables are inserted into the output CSS document.

For example:

```
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100%$font-stack;
  color: $primary-color;
}
```

For more information on Sass, see the [Sass/SCSS reference](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#operations).

## SCSS functions

List of functions for Service Portal SCSS compiler.

### RGB functions

|Function|Description|
|--------|-----------|
|rgb\($red, $green, $blue\)|Creates a Color from red, green, and blue values.|
|rgba\($red, $green, $blue, $alpha\)|Creates a Color from red, green, blue, and alpha values.|
|red\($color\)|Gets the red component of a color.|
|green\($color\)|Gets the green component of a color.|
|blue\($color\)|Gets the blue component of a color.|
|mix\($color1, $color2, \[$weight\]\)|Mixes two colors together.|

### HSL functions

|Function|Description|Availability|
|--------|-----------|------------|
|hsl\($hue, $saturation, $lightness\)|Creates a Color from hue, saturation, and lightness values.|Yes|
|hsla\($hue, $saturation, $lightness, $alpha\)|Creates a Color from hue, saturation, lightness, and alpha values.|Yes|
|hue\($color\)|Gets the hue component of a color.|Yes|
|saturation\($color\)|Gets the saturation component of a color.|Yes|
|lightness\($color\)|Gets the lightness component of a color.|Yes|
|adjust-hue\($color, $degrees\)|Changes the hue of a color.|Yes|
|lighten\($color, $amount\)|Makes a color lighter.|Yes|
|darken\($color, $amount\)|Makes a color darker.|Yes|
|saturate\($color, $amount\)|Makes a color more saturated.|Yes|
|desaturate\($color, $amount\)|Makes a color less saturated.|Yes|
|grayscale\($color\)|Converts a color to grayscale.|Yes|
|complement\($color\)|Returns the complement of a color.|No|
|invert\($color\)|Returns the inverse of a color.|No|

### Opacity functions

|Function|Description|Availability|
|--------|-----------|------------|
|alpha\($color\)|Gets the alpha component \(opacity\) of a color.|Yes|
|opacity\($color\)|Gets the alpha component \(opacity\) of a color.|Yes|
|rgba\($color, $alpha\)|Changes the alpha component for a color.|Yes|
|opacify\($color, $amount\)|Makes a color more opaque.|No|
|fade-in\($color, $amount\)|Makes a color more opaque.|No|
|transparentize\($color, $amount\)|Makes a color more transparent.|No|
|fade-out\($color, $amount\)|Makes a color more transparent.|No|

### Other color functions

|Function|Description|Availability|
|--------|-----------|------------|
|adjust-color\(\)|Increases or decreases one or more components of a color.|Yes|
|scale-color\(\)|Fluidly scales one or more properties of a color.|Yes|
|change-color\(\)|Changes one or more properties of a color.|No|
|ie-hex-str\(\)|Converts a color into the format understood by IE filters.|No|

### String functions

|Function|Description|Availability|
|--------|-----------|------------|
|unquote\($string\)|Removes quotes from a string.|Yes|
|quote\($string\)|Adds quotes to a string.|Yes|
|str-length\($string\)|Returns the number of characters in a string.|No|
|str-insert\($string, $insert, $index\)|Inserts $insert into $string at $index.|No|
|str-index\($string, $substring\)|Returns the index of the first occurrence of $substring in $string.|No|
|str-slice\($string, $start-at, \[$end-at\]\)|Extracts a substring from $string.|No|
|to-upper-case\($string\)|Converts a string to upper case.|No|
|to-lower-case\($string\)|Converts a string to lower case.|No|

### Number functions

|Function|Description|Availability|
|--------|-----------|------------|
|percentage\($number\)|Converts a unitless number to a percentage.|Yes|
|round\($number\)|Rounds a number to the nearest whole number.|Yes|
|ceil\($number\)|Rounds a number up to the next whole number.|Yes|
|floor\($number\)|Rounds a number down to the previous whole number.|Yes|
|abs\($number\)|Returns the absolute value of a number.|Yes|
|min\($numbers…\)|Finds the minimum of several numbers.|Yes|
|max\($numbers…\)|Finds the maximum of several numbers.|Yes|
|random\(\[$limit\]\)|Returns a random number.|No|

### List functions

Lists in SCSS are immutable. All list functions return a new list rather than updating the existing list in-place.

All list functions work for maps as well, treating them as lists of pairs.

|Function|Description|
|--------|-----------|
|length\($list\)|Returns the length of a list.|
|nth\($list, $n\)|Returns a specific item in a list.|
|set-nth\($list, $n, $value\)|Replaces the nth item in a list.|
|join\($list1, $list2\)|Joins two lists into one.|
|append\($list1, $val\)|Appends a single value onto the end of a list.|
|zip\($lists…\)|Combines several lists into a single multidimensional list.|
|index\($list, $value\)|Returns the position of a value within a list.|
|list-separator\($list\)|Returns the separator of a list.|

### Adding custom functions

**Scss @function my-calculation-function\($some-number, $another-number\)\{ @return $some-number + $another-number \}**

## SCSS nesting

SCSS lets you nest your CSS selectors in a way that follows the same visual hierarchy of your HTML.

For example:

```
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

The `ul`, `li`, and `a` selectors are nested inside the `nav` selector, which is a great way to organize your CSS and make it more readable. When the widget is rendered, the generated CSS looks something like the following code block:

```
nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

nav li {
  display: inline-block;
}

nav a {
  display: block;
  padding: 6px 12px;
  text-decoration: none;
}
```

For more information on Sass, see the [Sass/SCSS reference](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#operations).

## SCSS operators

SCSS has a handful of standard math operators like +, -, \*, /, and %.

Use simple math to calculate widths for an aside `&` article. For example:

```
.container { width: 100%; }

article[role="main"] {
  float: left;
  width: 600px / 960px * 100%;
}

aside[role="complementary"] {
  float: right;
  width: 300px / 960px * 100%;
}
```

The generated CSS looks like:

```
.container {
  width: 100%;
}

article[role="main"] {
  float: left;
  width: 62.5%;
}

aside[role="complementary"] {
  float: right;
  width: 31.25%;
}
```

For more information on Sass, see the [Sass/SCSS reference](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#operations).

## SCSS mixins

A mixin lets you make groups of CSS declarations that you want to reuse throughout your site. You can pass in values to make your mixin more flexible.

The following code block is an example for border-radius.

```
@mixin border-radius($radius) {
  -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
      -ms-border-radius: $radius;
          border-radius: $radius;
}

.box { @include border-radius(10px); }
```

The generated CSS looks like:

```
.box {
  -webkit-border-radius: 10px;
  -moz-border-radius: 10px;
  -ms-border-radius: 10px;
  border-radius: 10px;
}
```

For more information on Sass, see the [Sass/SCSS reference](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#operations).

