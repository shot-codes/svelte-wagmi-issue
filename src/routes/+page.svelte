<script lang="ts">
  import {
    WC,
    connected,
    signerAddress,
    disconnectWagmi,
  } from "svelte-wagmi";
</script>

<h1>Welcome to SvelteKit</h1>
<p>
  Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation
</p>

{#if $connected}
  <h1>{$signerAddress}</h1>
  <button on:click={disconnectWagmi}>disconnect</button>
{:else}
  <button on:click={WC}>walletconnect connect</button>
{/if}
