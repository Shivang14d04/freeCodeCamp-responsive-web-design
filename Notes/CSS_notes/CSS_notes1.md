# CSS NOTES - 1

## Step 1

CSS (Cascading Style Sheets)is the language used to style an HTML document. It describes how HTML elements should be displayed on the screen.

there is a basic structure needed to start building your web page. Every HTML document should have a DOCTYPE declaration and html element. The DOCTYPE tells the browser which version of HTML the document is in. And the html element represents the root element which contains all other elements.
Example Code

```html
<!DOCTYPE html>
<html lang="en">
  <!--all other elements go here-->
</html>
```

# Step 2

You can add style to an element by specifying it in the style element(made in head element) and setting a property for it like this:

Example Code

```html
element { property: value; }
<style>
  h1 {
    text-align: center;
  }
</style>
```

# Step 3

You can add the same group of styles to many elements by creating a list of selectors. Each selector is separated with commas like this:

Example Code

```
selector1, selector2 {
property: value;
}
```

# Step 4

You have styled three elements by writing CSS inside the style tags. This works, but since there will be many more styles, it's best to put all the styles in a separate file and link to it.

Now you need to link the styles.css file. Inside the head element, add a link element. Give it a rel attribute with the value of "stylesheet" and an href attribute with the value of "styles.css".

Note that the link element is a void element.

```html
<head>
  <link rel="stylesheet" href="styles.css" />
  <meta charset="utf-8" />
  <title>Cafe Menu</title>
</head>
```

# Step 5

For the styling of the page to look similar on mobile as it does on a desktop or laptop, you need to add a meta element with a special content attribute.

Example Code

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

# Step 6

The div element is used mainly for design layout purposes, unlike the other content elements you have used so far.

```html
<div id="menu">
  <main>
    <h1>CAMPER CAFE</h1>
    <p>Est. 2020</p>
    <section>
      <h2>Coffee</h2>
    </section>
  </main>
</div>
```

# Step 7

now to make the div not take up the entire width of the page. The CSS width property is perfect for this.

You can use the id selector to target a specific element with an id attribute. An id selector is defined by placing the hash symbol # directly in front of the element's id value. For example, if an element has the id of cat then you would target that element like this:

```css
#cat {
  width: 250px;
}
```

# Step 8

px is a fixed unit → doesn't adapt to screen size.

% is relative to the parent → more responsive.

Makes layout adjust better on different devices or window sizes.
for example

```css
#menu {
  width: 80%; /* Relative to the parent element's width */
  text-align: center;
}
```

# Step 9

Next, You can center the item horizontally by setting its margin-left and margin-right properties to auto. Think of the margin as an invisible space around an element. Using these two margin properties, center the #menu element within the body element.

```css
#menu {
  width: 80%;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
}
```

# Step 10

you could use an image of your own choice as the page background.

to do so ,add a background-image property and set its value to url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg) (image path).

article elements commonly contain multiple elements that have related information. I

# Step 11

p elements are block-level elements, so they take up the entire width of their parent element.

To get them on the same line, you need to apply some styling to the p elements so they behave more like inline elements.you can do this by display property and set it to inline-block.
inline-block elements only take up as much horizontal space as their content requires — no more, no less.
By default, an inline-block element:

Does not stretch to fill the container.

Only occupies the space needed by its content.

You can manually set the width if needed.

# Step 12

The max-width property sets the maximum width an element can grow to, regardless of the content size or screen width.
Prevents elements from becoming too wide on large screens

Helps create responsive layouts

Often used with width: 100% to allow flexibility within limits.

# Step 13

You can add a fallback value for the font-family by adding another font name separated by a comma. Fallbacks are used in instances where the initial is not found/available.
example

```css
h1,
h2 {
  font-family: Impact, serif;
}
```

# Step 14

The typography of heading elements (e.g. h1, h2) is set by default values of users' browsers.
you can change it bu using font-size property.

```css
h1 {
  font-size: 40px;
}
h2 {
  font-size: 30px;
}
```

# Step 15

The default color of a link that has not yet been clicked on is typically blue. The default color of a link that has already been visited from a page is typically purple.

```css
a {
  color: black;
}
```

You change the properties of a link when the link has actually been visited by using a pseudo-selector that looks like a:visited { propertyName: propertyValue; }.

```css
a:visited {
  color: grey;
}
```

You change the properties of a link when the mouse hovers over them by using a pseudo-selector that looks like a:hover { propertyName: propertyValue; }.

You change the properties of a link when the link is actually being clicked by using a pseudo-selector that looks like a:active { propertyName: propertyValue; }.

# Step 16

Browsers apply default margin and padding to certain HTML elements like <h1>, <p>, and <ul>.
This can create unwanted spacing in your layout, especially at the top and bottom of elements.
For consistent layout control
use margin:0;

# Step 17

Sometimes elements (like <h2> and <img>) have too much vertical space between them due to default margins applied by the browser.
Common Solutions:
Option 1: Adjust Element Margins Directly
Reduce or remove the bottom margin of the text element (e.g., <h2>)

Option 2: Use Negative Top Margin on the Next Element
Pull the next element (like an image) upward by applying a negative margin-top:
