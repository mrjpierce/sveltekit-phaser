<script lang="ts">
    import { onMount } from 'svelte';
    
    onMount(async () => {
        const Phaser = await import('phaser');
        const config = (await import('./config')).default;
        const Demo = (await import('./scenes/Game')).default;
    
        new Phaser.Game({
            ...config,
            scene: [Demo]
        });
    });
</script>

<svelte:head>
	<title>Sveltekit + Phaser</title>
	<meta name="Sveltekit + Phaser" content="An example of using phaser with sveltekit" />
</svelte:head>

<div id="game"></div> 
