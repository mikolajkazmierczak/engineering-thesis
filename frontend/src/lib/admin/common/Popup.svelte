<script>
  import { fade, fly } from 'svelte/transition';
  import { createEventDispatcher } from 'svelte';
  import Button from '@c/Button.svelte';

  const dispatch = createEventDispatcher();

  export let title;
  export let opened;
  export let maxWidth = '500px';

  function close() {
    opened = false;
    dispatch('close');
  }
</script>

{#if opened}
  <div class="wrapper" transition:fade={{ duration: 200 }} on:click|self={close}>
    <div class="content" transition:fly={{ duration: 300 }} style:max-width={maxWidth}>
      <div class="close">
        <Button icon="close" on:click={close} square />
      </div>
      <h3>{title}</h3>
      <slot />
    </div>
  </div>
{/if}

<style>
  .wrapper {
    position: fixed;
    z-index: 1000;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: grid;
    place-items: center;
    background-color: rgba(0, 0, 0, 0.5);
  }
  .content {
    position: relative;
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    padding: 2rem;
    border-radius: var(--border-radius);
    border: var(--border);
    background-color: var(--light);
  }
  .close {
    position: absolute;
    top: -0.5rem;
    right: -0.5rem;
  }
</style>
