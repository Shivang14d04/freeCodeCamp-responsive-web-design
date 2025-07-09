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
