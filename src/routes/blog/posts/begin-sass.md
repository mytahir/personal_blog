---
title: Tips for learning SCSS/ sass (as a beginner) 
date: "2019-05-12T08:38:00.000Z"
---

I've been learning and working with SCSS/ sass for about 3 months in personal and professional projects. If you're not familiar, SCSS and sass are CSS pre-processors; at a basic level these are languages that get compiled and formatted into regular CSS that can be read by a web browser. 

<!-- more -->
![Sass Logo](https://images.iambacon.co.uk/blog/sass.png)

The advent of this technology took the very tedious task of writing CSS and made it a more modern and far more efficient process. Pre-processors allow things like variables, partials, nesting and mixins to be used in writing CSS styles. Not only does this cut down on code, it also enhances the developer experience a great deal (IMHO).

As someone who is relatively new to this technology, I thought I'd share some things that I wish I would have known before I started. If you'd like a run down on all of the features of sass, look [here](https://sass-lang.com/guide). 

##Learn how to stay organized
Before you even begin learning any CSS pre-processor, I recommend learning how to best structure and organize your CSS. With the module system that's built into sass, you're eventually going to be splitting your styles into different files all together. If you don't have organization conventions, I find it very easy to get lost in your file system. 

##Remember how the compiler works & break it down
If I had to give you one piece of advice to help you learn sass, it would be this: remember that the sass compiler will not only compile sass; it also compiles regular css. When I was first looking through the documentation for sass, I was overwhelmed to say the least. The thing I found most helpful was to try and gain a good understand of one sass feature and then move onto the next one. I started with variables (IMHO the best place to start for beginners); then I wanted a way to store all of my variables in a separate file so I dove into partials, and so on...

##Practice IRL
As with anything code related, the best way to learn is to practice (duh); however I hate coding exercises. This is why I've found it far more helpful to throw sass into my projects. If you use the above approach, implementing sass into any of your current projects should be a breeze. Some other things I did to start off my initial learning was finding code pens I liked and attempting to convert parts of it to use sass. Most importantly, remember to practice on actual projects in the context you would normally be working in.