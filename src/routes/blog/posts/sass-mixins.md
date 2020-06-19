---
title: Examples of Sass/ SCSS Mixins 
date: "2019-05-25T07:38:00.000Z"
---

when I first started learning Sass, I had a hard time conceptualizing what a mixin was and what their uses were in the css I was writing. 
<!-- more -->
Now that I've been using mixins for a while, I thought I'd write a post showing some examples of really nice use cases for mixins. 

The first time it really hit me was when I realized I could use a mixin to minimize my code for working with *flexbox*...

###Example 1: Flexbox

I found myself writing this multiple time throughout all of my projects:
```css
.element{
    display:flex;
    flex-direction:row;
    justify-content:center;
    align-items:center;
}
```
This made my code very WET and very hard to manage. This is where the advantage of mixins became clear! By declaring this mixin...
```scss
@mixin flex ($direction, $justify, $align){
    display:flex;
    flex-direction:$direction;
    justify-content:$justify;
    align-items:$align;
}
```
calling the four most common rules in flexbox becomes this...
```scss
.element{
    @include flex(row, center, center);
}
```

###Example 2: Fade

Another habit I found myself developing was importing all of jQuery only to find myself using just fadeIn and fadeOut in my projects. This mixin allows a modular way to fade in and out elements using only CSS...
```scss
@mixin fade($fade, $timing, $length, $count, $fill){ 
        animation: $fade $timing $length;
        animation-iteration-count: $count; 
        animation-fill-mode: $fill; 
    } 
    @keyframes fadeIn { 
        0% { opacity: 0; } 
        100% { opacity: 1; } 
    } 
    @keyframes fadeOut { 
        0% { opacity: 1; } 
        100% { opacity: 0; } 
    }
```
This approach relies heavily on the ability to pass params to mixins, making them super flexible and modular for code you repeat often! 

Now animating an element with fade in simply looks like this...
```scss
.element{
    @include fade(fadeIn, ease, 5s, 1, forward);
}
```

###Example 3: Fonts
I've found it useful to use the following mixin when I'm using a font in different areas across a project, but at a range of sizes, weights, and spacings. 
```scss
@mixin font($style, $weight, $height, $spacing){
        font-family: 'Jost', sans-serif;
        font-style: $style;
        font-weight: $weight;
        line-height: $height;
        letter-spacing: $spacing;
    }
```
So calling a font with all of these specifications looks like this...
```scss
.element{
    @include font(italic, 400, 1, 5px);
}
```
This can even be expanded a little more if you're using multiple fonts...

```scss
@mixin font($family, $category, $style, $weight, $height, $spacing){
        font-family: $family, $category;
        font-style: $style;
        font-weight: $weight;
        line-height: $height;
        letter-spacing: $spacing;
    }
```


###remember, 
*I'll be updating this article often as I write new and even better mixins!*

