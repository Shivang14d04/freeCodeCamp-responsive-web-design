# 1

The margin shorthand property makes it easy to set multiple margin areas at the same time.

To center your element on the page, set its margin property to auto. This sets margin-top, margin-right, margin-bottom, and margin-left all to auto.
When the shorthand margin property has two values, it sets margin-top and margin-bottom to the first value, and margin-left and margin-right to the second value.
example

```css
.marker {
  width: 200px;
  height: 25px;
  background-color: red;
  margin: 10px auto;
}
```

# 2

Multiple classes can be added to an element by listing them in the class attribute and separating them with a space. For example, the following adds both the animal and dog classes to a div element.
Example Code

```css
<div class="animal dog">
```

# 3

There are two main color models: the additive RGB (red, green, blue) model used in electronic devices, and the subtractive CMYK (cyan, magenta, yellow, black) model used in print.

Iyou'll work with the RGB model in css. This means that colors begin as black, and change as different levels of red, green, and blue are introduced. An easy way to see this is with the CSS rgb function.

example:

```css
.container {
  background-color: rgb(0, 0, 0);
}
```

# 4

A function is a piece of code that can take an input and perform a specific action. The CSS rgb function accepts values, or arguments, for red, green, and blue, and produces a color:

Example Code

```css
rgb(red, green, blue);
```

Each red, green, and blue value is a number from 0 to 255. 0 means that there's 0% of that color, and is black. 255 means that there's 100% of that color.

In the additive RGB color model, primary colors are colors that, when combined, create pure white. But for this to happen, each color needs to be at its highest intensity.

# 5

Secondary colors are the colors you get when you combine primary colors. You might have noticed some secondary colors in the last step as you changed the red, green, and blue values.

In the RGB color model, which is used in digital displays and web design, secondary colors are created by combining two primary colors (Red, Green, Blue) at full intensity (255), while the third remains at 0.

🌈 Secondary Colors in RGB:
Yellow = Red + Green → rgb(255, 255, 0)

Cyan = Green + Blue → rgb(0, 255, 255)

Magenta = Red + Blue → rgb(255, 0, 255)

# 6

In the RGB color model, tertiary colors are made by combining a primary color with a neighboring secondary color—this involves mixing unequal intensities of two primary colors.

🌗 Tertiary Color: Orange
Orange is made by mixing Red (primary) with Yellow (secondary).

In RGB:

Red is maxed out at 255

Green is set to a medium value like 127

Blue remains 0

# 7

Complementary colors are pairs of colors that are directly opposite each other on the color wheel. In the RGB model, these color pairs create high contrast and can appear very vibrant when used side by side.

Using complementary colors together at full brightness (like red and cyan) can cause visual strain and make text difficult to read, especially for people with visual sensitivities.

Use one color as the dominant (main) color for backgrounds or large sections.

Use its complementary color as an accent — for example, in buttons, links, highlights, or calls to action — to draw attention without overwhelming the user.

# 8

A very common way to apply color to an element with CSS is with hexadecimal or hex values. While hex values sound complicated, they're really just another form of RGB values.

Hex color values start with a # character and take six characters from 0-9 and A-F. The first pair of characters represent red, the second pair represent green, and the third pair represent blue. For example, #4B5320.

for example

```css
.green {
  background-color: #00ff00;
}
```

You may already be familiar with decimal, or base 10 values, which go from 0 - 9. Hexadecimal, or base 16 values, go from 0 - 9, then A - F:

Example Code

```
0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F
```

With hex colors, 00 is 0% of that color, and FF is 100%. So #00FF00 translates to 0% red, 100% green, and 0% blue, and is the same as rgb(0, 255, 0).

# 9

The HSL color model, or hue, saturation, and lightness, is another way to represent colors.

The CSS hsl function accepts 3 values: a number from 0 to 360 for hue, a percentage from 0 to 100 for saturation, and a percentage from 0 to 100 for lightness.

If you imagine a color wheel, the hue red is at 0 degrees, green is at 120 degrees, and blue is at 240 degrees.

Saturation is the intensity of a color from 0%, or gray, to 100% for pure color. You must add the percent sign % to the saturation and lightness values.

Lightness is how bright a color appears, from 0%, or complete black, to 100%, complete white, with 50% being neutral.

for example

```css
.blue {
  background-color: hsl(240, 100%, 50%);
}
```

# 10

A gradient is when one color transitions into another. The CSS linear-gradient function lets you control the direction of the transition along a line, and which colors are used.

One thing to remember is that the linear-gradient function actually creates an image element, and is usually paired with the background property which can accept an image as a value.

The linear-gradient function is very flexible -- here is the basic syntax you'll use in this tutorial:

Example Code

```css
linear-gradient(gradientDirection, color1, color2, ...);
```

gradientDirection is the direction of the line used for the transition. color1 and color2 are color arguments, which are the colors that will be used in the transition itself. These can be any type of color, including color keywords, hex, rgb, or hsl.

While the linear-gradient function needs a minimum of two color arguments to work, it can accept many color arguments.

example

```css
.red {
  background: linear-gradient(
    90deg,
    rgb(255, 0, 0),
    rgb(0, 255, 0),
    rgb(0, 0, 255)
  );
}
```

Color-stops allow you to fine-tune where colors are placed along the gradient line. They are a length unit like px or percentages that follow a color in the linear-gradient function.

For example, in this red-black gradient, the transition from red to black takes place at the 90% point along the gradient line, so red takes up most of the available space:

Example Code

```css
linear-gradient(90deg, red 90%, black);
```

# 11

When using the linear-gradient() function in CSS without specifying color stops, the browser automatically places the colors evenly along the gradient line.

Default Behavior:
If you define two colors, the gradient smoothly transitions from the first color at 0% to the second at 100%.

If you define three colors, they are automatically placed at:

First color → 0% (start)

Second color → 50% (middle)

Third color → 100% (end)

If no gradientDirection argument is provided to the linear-gradient function, it arranges colors from top to bottom, or along a 180 degree line, by default.

# 12

With the CSS opacity property, you can control how opaque or transparent an element is. With the value 0, or 0%, the element will be completely transparent, and at 1.0, or 100%, the element will be completely opaque like it is by default.

Another way to set the opacity for an element is with the alpha channel. Similar to the opacity property, the alpha channel controls how transparent or opaque a color is.

You're already familiar with using the rgb function to set colors. To add an alpha channel to an rgb color, use the rgba function instead.

The rgba function works just like the rgb function, but takes one more number from 0 to 1.0 for the alpha channel:

Example Code

```css
rgba(redValue, greenValue, blueValue, alphaValue);
```

You can also use an alpha channel with hsl and hex colors.

the default display property for div elements is block. So when two block elements are next to each other, they stack like actual blocks. For example, your marker elements are all stacked on top of each other.

To position two div elements on the same line, set their display properties to inline-block.

Borders have several styles to choose from. You can make your border a solid line, but you can also use a dashed or dotted line if you prefer. Solid border lines are probably the most common.

```css
.sleeve {
  width: 110px;
  height: 25px;
  background-color: rgba(255, 255, 255, 0.5);
  border-left-width: 10px;
  border-left-style: solid;
}
```

The border-left shorthand property lets you to set the left border's width, style, and color at the same time.

Here is the syntax:

```css
border-left: width style color;
```

# 13

The last thing you'll do is add a slight shadow to each marker to make them look even more realistic.

The box-shadow property lets you apply one or more shadows around an element. Here is basic syntax:

Example Code

```css
box-shadow: offsetX offsetY color;
```

Here's how the offsetX and offsetY values work:

both offsetX and offsetY accept number values in px and other CSS units.
a positive offsetX value moves the shadow right and a negative value moves it left.
a positive offsetY value moves the shadow down and a negative value moves it up.
if you want a value of zero (0) for any or both offsetX and offsetY, you don't need to add a unit. Every browser understands that zero means no change.
The height and width of the shadow is determined by the height and width of the element it's applied to. You can also use an optional spreadRadius value to spread out the reach of the shadow. More on that later.

```css
box-shadow: offsetX offsetY blurRadius color;
```

If a blurRadius value isn't included, it defaults to 0 and produces sharp edges. The higher the value of blurRadius, the greater the blurring effect is.

```css
box-shadow: 5px 5px 5px green;
```

But what if you wanted to expand the shadow out further? You can do that with the optional spreadRadius value:

Example Code

```css
box-shadow: offsetX offsetY blurRadius spreadRadius color;
```

Like blurRadius, spreadRadius defaults to 0 if it isn't included.

# 14

The vh unit stands for viewport height, and is equal to 1% of the height of the viewport. This makes it relative to the viewport height.

The rem unit stands for root em, and is relative to the font size of the html element.

# 15

You can select the last element of a specific type using the last-of-type CSS pseudo-class, like this:

Example Code

```css
p:last-of-type {
}
```

That will select the last p element.

```css
fieldset:last-of-type {
  border-bottom: none;
}
```

# 16

To override a general rule like input { width: 100%; }, you can target a more specific class (e.g., .inline) and use width: unset;. This resets the width to its default value.

Example:

```css
.inline {
  width: unset;
}
```

# 17

Browsers apply default styles to HTML elements, which can vary slightly across browsers. For example, text input fields usually have default padding like 1px 2px, but file input fields may appear smaller because they don’t receive the same styling. To ensure consistency, it's common to reset or override these default styles using CSS.

```css
input[type="file"] {
  padding: 1px 2px;
}
```
