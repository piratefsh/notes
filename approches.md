# Approaches to CSS

# Start with good HTML
Use semantic tags (e.g. `article`, `header`, `section`) 

Structure things in the most meaningful way possible. use `nav` instead of `div` for a navigation bar. 

Keep your HTML as simple as possible. Start with the content that you need, style it, and only add elements if needed

# Important basics of CSS
## Box Model
* what is margin, padding, border and content, where does one begin and the other end?
* what is the `box-sizing` property, and when to use it?

## Display
* the differences between block, inline-block, inline, etc. 
* [flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) is super important to know too.

## Positioning
* what does relative, absolute and fixed positions mean?
* how to absolutely position an element in a relatively positioned parent?

# Organizing your identifiers
## id vs class
When to use id and when not to?

# vh and vw
How to set height and width relative to viewport

## Naming classes
* Use block-element-modifier style ([BEM](http://getbem.com/introduction/)) naming conventions 
    * Makes it easier to reuse code
    * Makes it easier to look for CSS snippets 

    e.g. all header related stuff will be under `.header` 

```css
.header 
    .header-logo
        color: blue
    .header-login-form
        display: inline-block
```

* Avoid using classes if possible (controversial)
    * Makes your HTML much cleaner
    * e.g. instead of:

```html
<ul class='people'>
    <li class='person'>Sher Minn</li>
    <li class='person'>Bigfoot</li>
</ul>

.people
    .person
        color: red
```

try:

```html
<ul class='people'>
   <li>Sher Minn</li>
    <li>Bigfoot</li>
</ul>

.people
    li
        color: red
```

* Use semantic class names (controversial)
    * e.g. instead of naming a class `red-button`, try `danger-button`
    * describe the role of the element rather than the style
    * worried about reusing code? use `mixins` instead


# Frameworks?
* Avoid Bootstrap or other frameworks for custom layouts
* Write your own layout style to get comfortable with positioning and displays

# Preprocessors
Use SASS/LESS instead of vanilla CSS. Why?
* Less math for you 
* Variables (omg)
* Helps with auto prefixing (-webkit, -moz, etc)
* Easier to chunk up CSS
