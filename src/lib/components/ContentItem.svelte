<script lang="ts">
  export let title: string;
  export let isOpen: boolean = false;
  export let previewUrl: string | undefined = undefined;
  export let linkUrl: string | undefined = undefined;
  export let imgSrc: string | undefined = undefined;

  function toggle() {
    isOpen = !isOpen;
  }
</script>

<article class="content-item" class:open={isOpen}>
  <button class="toggle-header" on:click={toggle} aria-expanded={isOpen}>
    <span class="toggle-icon">{isOpen ? "▼" : "▶"}</span>
    <h3>{title}</h3>
  </button>

  {#if isOpen}
    <div class="content-body">
      {#if linkUrl}
        <a href={linkUrl} target="_blank" rel="noopener noreferrer">
          {linkUrl}
        </a>
      {/if}

      <slot />

      {#if imgSrc}
        <img src={imgSrc} alt="" />
      {/if}

      {#if previewUrl}
        <a
          href={previewUrl}
          class="link-preview"
          target="_blank"
          rel="noopener noreferrer"
        >
          {previewUrl}
        </a>
      {/if}
    </div>
  {/if}
</article>

<style>
  .content-item {
    background: rgba(255, 255, 255, 0.5);
    border-radius: 10px;
    margin-bottom: 1rem;
    border: 2px solid rgba(210, 105, 30, 0.3);
    transition: all 0.2s ease;
  }

  .content-item:hover {
    border-color: rgba(210, 105, 30, 0.6);
    background: rgba(255, 255, 255, 0.7);
  }

  .toggle-header {
    width: 100%;
    margin: 0;
    padding: 1rem 1.5rem;
    background: none;
    border: none;
    color: #8b4513;
    font-size: 1.2rem;
    cursor: pointer;
    user-select: none;
    display: flex;
    align-items: center;
    gap: 0.5rem;
    transition: color 0.2s ease;
    text-align: left;
  }

  .toggle-header:hover {
    color: #d2691e;
  }

  .toggle-header:focus {
    outline: 2px solid #d2691e;
    outline-offset: 2px;
  }

  .toggle-header h3 {
    margin: 0;
    font-size: inherit;
    font-weight: bold;
    color: inherit;
  }

  .toggle-icon {
    font-size: 0.8em;
    transition: transform 0.2s ease;
    display: inline-block;
    min-width: 1em;
  }

  .content-body {
    padding: 0 1.5rem 1.5rem 1.5rem;
    color: #654321;
    animation: slideDown 0.2s ease-out;
  }

  @keyframes slideDown {
    from {
      opacity: 0;
      transform: translateY(-10px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  .content-body :global(p) {
    margin: 0 0 1rem 0;
    line-height: 1.6;
  }

  .content-body :global(p:last-child) {
    margin-bottom: 0;
  }

  .content-body :global(img) {
    max-width: 100%;
    height: auto;
    border-radius: 8px;
    margin: 1rem 0;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  }

  .content-body :global(a) {
    color: #d2691e;
    text-decoration: none;
    border-bottom: 1px solid rgba(210, 105, 30, 0.3);
    transition: all 0.2s ease;
  }

  .content-body :global(a:hover) {
    color: #8b4513;
    border-bottom-color: #8b4513;
  }

  .content-body :global(.link-preview) {
    display: block;
    padding: 1rem;
    background: rgba(255, 255, 255, 0.6);
    border-radius: 8px;
    border-left: 4px solid #d2691e;
    margin: 1rem 0;
    text-decoration: none;
  }

  .content-body :global(.chart-container) {
    margin: 1.5rem 0;
    padding: 1rem;
    background: rgba(255, 255, 255, 0.6);
    border-radius: 8px;
  }
</style>
