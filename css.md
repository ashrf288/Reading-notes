
# css:
### CSS syntax :
CSS is a rule-based language — you define rules specifying groups of styles that should be applied to particular elements or groups of elements on your web page. 

The rule opens with a **selector **. This selects the HTML element that we are going to style.
We then have a set of curly braces `{ }` Inside those will be one or more declarations, which take the form of **property and value pairs**.

example :

`h1 {`

`    color: red;`

`    font-size: 5em;`

`}`

### As there are so many things that you could style using CSS, the language is broken down into modules. 

## Three Ways to Insert CSS :
There are three ways of inserting a style sheet:

* **External CSS** :Each HTML page must include a reference to the external style sheet file inside the` <link> `element, inside the head section.

+ **Internal CSS** The internal style is defined inside the`<style>` element, inside the head section.
- **Inline CSS** To use inline styles, add the `style` attribute to the relevant element. The style attribute can contain any CSS property.

## If some properties have been defined for the same selector *element) in different style sheets, the value from the last read style sheet will be used. 

## some css property:
- CSS color Property: The `color` property specifies the color of text.

syntax : `color: color|initial|inherit;`.

## Selectors:
* **Basic selectors** are fundamental selectors; these are the most basic selectors that are frequently combined to create other, more **complex selectors.**
* **Grouping selectors** : Specifies that both A and B elements are selected. This is a grouping method to select several matching elements.
* **Combinators**
Combinators are selectors that establish a relationship between two or more simple selectors


