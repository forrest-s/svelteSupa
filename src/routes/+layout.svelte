<script>
    import '../styles.css'
    import Header from '$lib/components/Header.svelte'

    import { onMount } from 'svelte';
    import { supabaseClient } from '../lib/supabase';
    import { invalidateAll } from '$app/navigation';
    onMount(() => {
        const { data: { subscription }} = supabaseClient.auth.onAuthStateChange(() => {
            invalidateAll()
        })

        return () => { subscription.unsubscribe() }
    })
    
    
</script>

<Header />
<main class='flex justify-center mt-4'>
    <slot />
</main>