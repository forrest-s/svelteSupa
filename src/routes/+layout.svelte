<script>
    import '../styles.css'
    import Header from '$lib/components/Header.svelte'
</script>

<Header />
<main class='flex justify-center mt-4'>
    <slot />
</main>