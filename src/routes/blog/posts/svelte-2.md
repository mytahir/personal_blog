---
title: Learning Svelte 2 | data, templating & styling
date: "2020-06-29T12:47:00.000Z"
---

In this second article in a series on [Svelte.js](https://svelte.dev) we're going to cover the very basics of dynamic data in svelte, how to populate our template with said data, and how to style it all. First, lets look at the basics of how our data interacts with our template.

```svelte
	<script>
		let name = 'world';
	</script>
	
	<h1>Hello {name}!</h1>
```

In this little Hello World example, we see that all we have to do is save our data to a variable ('name') and place that variable inside of curly braces within our HTML template. If you've seen JS templating frameworks like Handlebars, this may look familiar. Obviously when you recieve any sort of real data from an API or database, it will likely be an array or object. We can use the following syntax to pull values from an array or object...

```svelte
	<script>
		let names = {
			one: 'megan',
			two: 'jeff',
			three: 'muhammad'
		};
	</script>
	
	<h1>Hello {names.one}!</h1>
	<h1>Hello {names.two}!</h1>
	<h1>Hello {names.three}!</h1>
```

You can now see how you might populate a page with different values from a database. I find this syntax very intuitive if you're coming from vanilla HTML/CSS/Javascript and this is your first framework. Last thing I want to cover in this article is styling components. We'll get into the component structure next time, but just know styling in Svelte is very easy, *as styles are scoped to the component*. You also have global styles available, but scoping the styles to the component removes a lot of code from the compiled app! 

```svelte
	<script>
		let names = {
			one: 'megan',
			two: 'jeff',
			three: 'muhammad'
		};
	</script>
	
	<h1 id="1">Hello {names.one}!</h1>
	<h1 id="2">Hello {names.two}!</h1>
	<h1 id="3">Hello {names.three}!</h1>
	
	<style>
		h1{
			color:red;
		}
		#2{
			color:green;
		}
		#3{
			color:blue;
		}
	</style>
```

Here I've added style to our previous example. Even though our first selector is an element selector, it will only apply to the ```<h1>``` tags within this component, not throughout the whole app. 

If you're interested in Svelte, make sure to check back for more articles exploring Svelte with me! Make sure to check out the tutorials and REPL at [svelte.dev](https://svelte.dev). 