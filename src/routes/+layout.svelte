<script lang="ts">
	import './layout.css';
	let { children } = $props();
</script>

<svelte:head>
  <link rel="icon" href="imgs/favicon.ico" />
  <link rel="icon" href="imgs/favicon.png" />
  <link rel="icon" href="imgs/favicon.svg" />
  <meta name="description" content="Loupe helps researchers build, visualize, and share the evidence behind an object's history, from its first known record to today." />
  <meta name="keywords" content="Loupe, tool, provenance, research">
  <meta name="author" content="Calibro" />
  <link rel="canonical" href="https://domain.ext" />
  <meta property="og:locale" content="en_US" />
  <meta property="og:type" content="website" />
  <meta property="og:title" content="Loupe - A tool to structure and visualize provenance research" />
  <meta property="og:description" content="Loupe helps researchers build, visualize, and share the evidence behind an object's history, from its first known record to today." />
  <meta property="og:url" content="https://domain.ext/" />
  <meta property="og:site_name" content="Loupe - A tool to structure and visualize provenance research" />
  <meta property="og:image" content="imgs/og-img.jpg" />
  <meta name="apple-mobile-web-app-title" content="Loupe" />
  <meta name="application-name" content="Loupe" />
  <meta name="msapplication-TileColor" content='#FFFFFF' />
</svelte:head>

{@render children()}
