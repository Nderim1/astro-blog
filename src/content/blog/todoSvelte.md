---
author: devthoughts
title: Trying out SvelteJS
date: 2022-04-03T17:15:00Z
description: In an attempt to start learning Svelte, I decided to build a TODO app with it. Check out how I did!
tags:
  - coding
  - frameworks
  - svelte
  - todo
postSlug: try-sveltejs
ogImage: assets/images/svelte-todo.png
---

![Test image](/public/assets/images/svelte-todo.png)

[DEMO App](https://svelte.devthoughts.xyz)  
[Source Code](https://github.com/Nderim1/svelteTodo)

<br>

## What & Why

Today I will be building a simple but complete TODO app with SvelteJS.
A TODO app is fairly simple to build. You don't need to know complex concepts of the language to build such an app, which makes it the perfect thing to build when trying to learn or exploring a new language or framework. <br>
<a href='/posts/todo'>In this post</a> you can find a more extensive explanation of how the app will work.

## HOW

Svelte documentation is AMAZING!
I manage to build the whole app by just following [the examples on Svelte documentation page](https://svelte.dev/examples)!

One thing that you immediately notice when you start working with Svelte is how small the boilerplate code is. You can just create a file with `.svelte` and start writing HTML (not exactly tho since the "HTML" syntax you write in a .svelte file is a superset of HTML). <br>
How cool is that?

To add Javascript (and make use of Svelte features) you just need to add a `<script>` tag and you are good to go.

Same with styles: just add a `<style>` tag and start writing css.

I would not want learn Svelte as my first Javascript framework tho. Svelte does a lot of things under the hood that you might not understand if it is your first framework you learn. A lot of things are hidden underneath, and a lot of magic is going around.

Example: In React you use `export default MyComponent` to export a component. In Svelte you don't need that.

As soon as your create a file with `.svelte` extension, the Svelte compiler exports it automatically.

Passing a prop to a component is "interesting" in a weird way in Svelte.

Say you have a variable called `hello` that you want to pass down to a child component:

```svelte
<script>
  import ChildComponent from './ChildComponent.svelte';
  const hello = 'hello';
</script>

< ChildComponent hello={hello} />
```

In the child component then you need to use, brace yourself, the `export` keyword to accept the prop:

```svelte
// ChildComponent.svelte

<script>
  export let hello;
</script>

<span>{hello} there</span>
```

WAT? :D Anywaysss...

State in Svelte is a piece of cake. At least the variation of it with no stores involved.

You just declare a variable in the script tag and use it wherever you want in the file. The component will get rerendered when that variable changes.

Nice stuff!

Overall I really like Svelte. I hope I will get the chance to create something more complex with it. You should try it too! :)
