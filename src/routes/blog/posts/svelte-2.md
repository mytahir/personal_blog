---
title: Learning Svelte 2 | Reactivity in Svelte 
date: "2020-06-21T12:47:00.000Z"
---

<!-- more -->


```
<script>
	let count = 0;

	function handleClick() {
		count += 1;
	}
</script>

<button on:click={ handleClick }>
	Clicked { count } { count === 1 ? 'time' : 'times' }
</button>
```