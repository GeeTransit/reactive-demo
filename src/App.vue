<script setup>
import { ref } from 'vue';
let count = ref(0);
</script>

<template>
	<header>
		<h1>George Zhang @ TMU</h1>

		<nav>
		<ul class="top-nav">
			<li><a href="https://cs.torontomu.ca/~gszhang/">Homepage</a></li>
		</ul>
		</nav>
	</header>

	<hr>

	<nav>
	<details>
		<summary>Table of Contents</summary>

		<ul class="nav">
			<li><a href="#demo">Reactive Counter Demo</a></li>
			<li><a href="#installation">Installation</a></li>
			<li><a href="#build">Build</a></li>
			<li><a href="#difficulties">Difficulties</a></li>
		</ul>
	</details>
	</nav>

	<main>
	<article>
		<h2>Reactive Web Pages with VueJS</h2>

		<section id="demo">
			<h3>Reactive Counter Demo</h3>

			<p>The count is {{ count }}.</p>

			<button v-on:click="count++">Increment</button>
		</section>

		<section id="installation">
			<h3>Installation</h3>

			<p>Installing VueJS was surprisingly simple. I created a new project using <code>npm create vue@latest</code>, installed dependencies using <code>npm install</code>, and ran the development server using <code>npm run dev</code>. The hot reload was unexpected but very useful in speeding up the development cycle.</p>
		</section>

		<section id="build">
			<h3>Build</h3>

			<p>Building the site was also very easy. I ran <code>npm run build</code> which output the built files into the <em>dist</em> folder. Running <code>npm run preview</code> allowed me to preview the built files (alternatively I could have opened the <em>index.html</em> file manually. I uploaded this folder onto Github Pages to host it.</p>
		</section>

		<section id="difficulties">
			<h3>Difficulties</h3>

			<p>I had some difficulty getting the counter to work right. Initially, I followed the example and made the counter take in a prop from the app but I got an error saying that the prop was readonly. I then looked at another example and it used data instead of prop. I switched it out and it worked perfectly. I had a few typos too (v-bind instead of v-on and onclick instead of click) but they were relatively easy to fix.</p>

			<p>I wanted to have a <cite>lab10c.html</cite> in my site (which would be the same as <cite>index.html</cite>) but it was very difficult to find resources on how to do that. VueJS was designed mostly for single page applications (SPA) where all the logic is in one page, reducing the amount of times a complex web application needs to fetch sites from the server. Eventually, I found a <a href="https://stackoverflow.com/questions/65868976/how-to-build-a-multi-pages-application-by-vite2-and-vue3/65884056#65884056">Stack Overflow answer on how to build multiple files</a> which involved configuring RollupJS and that did the trick.</p>

			<p>Deploying didn't come without surprises too. Because I was using Github Pages to host the site, the path was at <cite>/reactive-demo/lab10c.html</cite>, not <cite>/lab10c.html</cite>. I had to change a few paths and update the Vite configuration to output relative paths.</p>
		</section>
	</article>
	</main>

	<hr>

	<footer>
		<h2>Contact Info</h2>

		<p>George Zhang (he/him)<br>
		Toronto Metropolitan University<br>
		Faculty of Science<br>
		Computer Science Major<br>
		Bachelor of Science, Honours</p>

		<p>Email: <a href="mailto:george.zhang@torontomu.ca">george.zhang@torontomu.ca</a></p>
	</footer>
</template>

<style scoped>
</style>
