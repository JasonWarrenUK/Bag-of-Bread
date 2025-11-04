<script lang="ts">
  export let icon: string;
  export let title: string;
  export let strapline: string;
</script>

<section class="card">
  <header class="section-header">
    <div class="section-title">
      <div class="card-icon">{icon}</div>
      <h2>{title}</h2>
    </div>
    <div class="section-strapline">
      <p>{strapline}</p>
    </div>
  </header>
  <div class="section-content">
    <slot />
  </div>
</section>

<style>
  .card {
    background: rgba(255, 248, 220, 0.9);
    padding: 2rem;
    border-radius: 15px;
    transition: all 0.3s ease;
    border: 3px solid #daa520;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }

  .card:hover {
    transform: translateY(-8px) rotate(2deg);
    box-shadow: 0 12px 20px rgba(0, 0, 0, 0.2);
  }

  .section-header {
    text-align: center;
  }

  .section-title {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    margin-bottom: 1rem;
  }

  .card-icon {
    font-size: 2.5rem;
    filter: drop-shadow(2px 2px 4px rgba(0, 0, 0, 0.2));
    line-height: 1;
  }

  h2 {
    color: #8b4513;
    margin: 0;
    font-size: 1.5rem;
    line-height: 1;
  }

  .section-strapline {
    margin-bottom: 1rem;
  }

  .section-strapline p {
    color: #a0522d;
    margin: 0;
    line-height: 1.6;
  }

  .section-content {
    margin-top: 1.5rem;
  }

  .section-content:empty {
    display: none;
  }
</style>
