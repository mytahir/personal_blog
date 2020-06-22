---
title: Learning Svelte #1 | why you should too 
date: "2020-06-21T12:47:00.000Z"
---

After spending the last month scared of diving into a javascript framework, this week I found out about Svelte.js. I'd like to tell you why I think it's a great option for beginner javascript developers who are new to component/ module based javascript development. 
<!-- more -->
After spending the last month scared of diving into a javascript framework, this week I found out about [Svelte.js](https://svelte.dev). I'd like to tell you why I think it's a great option for beginner javascript developers who are new to component/ module based javascript development. 

If you're not familiar with Svelte, it works a little differently than other frameworks like React. Library based frameworks like React do a lot of the heavy lifting in the clients browsers as they receive it. Svelte, however, is a *compiler* **not a library**. This means that when you build your app, Svelte will take the project and convert it to plain HTML & vanilla JS. This means that the client only sees optimized (and mostly static) code, in much smaller bundles than a library based framework. This blog for example is built using Svelte and its SSG counter part [Sapper](sapper.svelte.dev). We'll get into Sapper in a later post, but just know, Sapper brings a lot to Svelte; things like routing, SSR, code splitting, and more! This blog is hosted on Github, which is then built and served on Netlify's CDN. This setup make continuous deployment a breeze, and lets me have a super fast personal site. 

Let's take a look at a basic Svelte component so we can ration with the syntax...

```svelte
	<script>
		let name = 'world';
	</script>
	
	<h1>Hello { name }</h1>
```

Here we can already see the simplicity of Svelte. a typical component consists of three parts...

```
	<script>
		javascript
	</script>
	
	<h1> markup </h1>
	
	<style>
		css
	</style>
```
The order of these doesn't technically matter, however it's best practice to place your ```<script>``` at the top. This is where we'll do things like import other components, add our logic, pass props, etc. But more on that later! In our example Hello World component, we can also see how data from within our ```<script>``` is referenced in our markup. We simply add curly braces around the javascript we want to place within our markup. 

I want to save most of my examples for later posts where I can be more indepth but I want to show you one example of how we can use forEach within our markup template to create a dynamic experience. 

Let's say you're building an online publishing app and you want to build a drop down to filter posts by category. Obviously you want to make this dynamic so categories can be added or removed in the future. Here's how we'd accomplish this in Svelte. 
```
	<script>
		// example array or categories (likely from a database response)
		let cats = [
			politics,
			international, 
			sports,
			entertainment, 
			reviews,
			opinion
		];
	</script>
	
	<select>
		{#each cats as cat}
			<option value={ cat }>
				{ cat }
			</option>
		{/each}
	</select>
```

This is really what sold me on Svelte. Here the {#each} loop is creating elements dynamically using the sample data from our 'database'. This makes building dynamic, data rich user interfaces so quick and painless with Svelte. I do a lot of work in wordpress and this feel like if the post loop had a smarter & sexier brother.

Also, Svelte feels just like what beginners are already familiar with: HTML and Javascript. If you're like me and have been intimidated by JS frameworks, I highly recommend you give Svelte a try. The development experience is wonderful, the syntax is truely effortless, and the docs are some of the most accessible & well-crafted docs I've read yet. 

Bonus Points: Svelte is also built by the community and not by the hidious corp facebook so... 🙃






