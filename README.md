# Starter-kit
Place to begin with web projects with lots of useful bits already setup

####Credits:
* Based on the <a href="https://html5boilerplate.com/" target="_blank">HTML Boilerplate project</a>  
* Using the Guardian <a href="https://github.com/guardian/sass-mq" target="_blank">sass-mq project</a>  
* JS Structure developed by <a href="http://www.grantmorrison.net/" target="_blank">Grant Morrison</a> whilst working at <a href="http://www.readingroom.com/" target="_blank">Reading Room</a>  


### The Component Concept:

Ideally you should be trying to split your styling down based on the component that it's related to, if it's not related to the styling of a component then styling should go into main.scss in styles/scss/core

___

### Useful SCSS bits to remember

```css
&     /// inherit the name of the thing above

/// scss example

.class-name {
    &.state {
        // new state styling
        background: blue;
    }
    &:hover, &:focus {
        // hover and focus styling
        background: red;
    }
}

/// css output

.class-name.state {
  background: blue;
}
.class-name:hover, .class-name:focus {
  background: red;
}

```
  
//


```css
*     /// Apply styling to all elements
```
  
//
  

```css
* + * /// Lobotomised owl selector
```
^^ <a href="http://alistapart.com/article/axiomatic-css-and-lobotomized-owls" target="_blank">http://alistapart.com/article/axiomatic-css-and-lobotomized-owls</a>    

//

```css
div > a 
/// Select element right inside container
/// so here we would be styling all anchor tags directly inside divs
```
Example markup:
```html
<div>
    <a href="#na">Hi there</a> /// styling applied here
    <p>
        <a href="#na">Hello again</a> /// but not here
    </p> 
</div>
```

//

[Inception rule](http://thesassway.com/beginner/the-inception-rule) -- don’t go nest your scss more than four levels

//

```css
%container {
    display: block;
    width: 100%;
    margin: 0 auto;
    padding: 0 2em;
    max-width: 60em;
    * {
        max-width: 100%;
    }
}
```
^^ Useful method for:
- Ensuring content remains in central column
- Keep padding either side of content
- Constraint max width of content
- Stopping internal elements stretching past the width of the parent

N.B.  
Must be used with box-sizing: border-box;  
Use @extend to put styling on wrapper  

___


### Box-sizing: border-box;
Box-sizing issues will likely cause you a ton of headaches
usually it will make sense to set all box-sizing on the page to border-box
meaning that all borders and padding only fill inside the constraints of the box and don't increase it's width:  
<a href="http://css-tricks.com/" target="_blank">http://css-tricks.com/box-sizing/</a>  
<a href="http://css-tricks.com/" target="_blank">http://css-tricks.com/inheriting-box-sizing-probably-slightly-better-best-practice/</a>  


```css
html {
  box-sizing: border-box;
}
*, *:before, *:after {
  box-sizing: inherit;
}
```
___

## Resources:

<a href="http://caniuse.com/" target="_blank">http://caniuse.com/</a> -- really good for quickly checking whether that fancy thing you just found will work in ie8  
<a href="http://css-tricks.com/" target="_blank">http://css-tricks.com/</a> -- Chris Coyier is the man  
<a href="http://codepen.io/" target="_blank">http://codepen.io/</a> -- Some amazing examples of people doing stuff with HTML CSS and JS and an excellent way to present quick web ideas  
<a href="http://stackoverflow.com/" target="_blank">http://stackoverflow.com/</a> -- you will more than likely live on here, great community of people asking and answering questions  
  
<a href="http://jquery.com/" target="_blank">http://jquery.com/</a> -- this starter-kit already has jquery included, as you get more comfortable with javascript you'll start to discover how useful jquery can be  

<a href="http://alistapart.com/" target="_blank">http://alistapart.com/</a> -- interesting, useful articles on web tech  
<a href="https://prepros.io/" target="_blank">https://prepros.io/</a> -- preprossing scss, js and md files // beware of the multiple requests to buy!  