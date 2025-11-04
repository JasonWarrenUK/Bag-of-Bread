<script lang="ts">
  import SectionCard from "$lib/components/SectionCard.svelte";
  import ContentItem from "$lib/components/ContentItem.svelte";

  let title = "Welcome to Bag of Bread!";
</script>

<svelte:head>
  <title>Bag of Bread - Crumbs and Nuggets</title>
  <meta
    name="description"
    content="A collection of resources and information, baked to perfection"
  />
</svelte:head>

<div class="home">
  <div class="hero">
    <h1>{title}</h1>
    <p class="subtitle">
      Your go-to source for deliciously random crumbs of wisdom
    </p>
  </div>

  <div class="content-grid">
    <SectionCard
      icon="🥖"
      title="Fresh Content"
      strapline="Hot out of the oven and ready to consume"
    >
      <ContentItem title="Latest Updates">
        <p>Check out our newest additions to the collection. Fresh daily!</p>
      </ContentItem>
      <ContentItem title="Today's Special">
        <p>Handpicked resources just for you.</p>
        <p>Because everyone deserves a little extra butter on their bread.</p>
      </ContentItem>
    </SectionCard>

    <SectionCard
      icon="🥐"
      title="Flaky Resources"
      strapline="Layered with knowledge and buttery smooth"
    >
      <ContentItem title="Learning Materials">
        <p>
          Delicate layers of information, carefully crafted for your
          consumption.
        </p>
      </ContentItem>
      <ContentItem title="Reference Guides">
        <p>Quick references when you need them most.</p>
      </ContentItem>
    </SectionCard>

    <SectionCard
      icon="🥯"
      title="Well-Rounded Info"
      strapline="Everything you knead to know"
    >
      <ContentItem title="Complete Resources">
        <p>A perfectly balanced collection of everything you might need.</p>
      </ContentItem>
      <ContentItem title="Tips & Tricks">
        <p>Little nuggets of wisdom to make your life easier.</p>
      </ContentItem>
    </SectionCard>
  </div>
</div>

<style>
  .home {
    animation: fadeIn 0.5s ease-in;
  }

  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  .hero {
    text-align: center;
    padding: 3rem 1rem;
    background: rgba(255, 255, 255, 0.8);
    border-radius: 20px;
    margin-bottom: 3rem;
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
    border: 4px dashed #d2691e;
  }

  h1 {
    font-size: 3rem;
    color: #8b4513;
    margin: 0 0 1rem 0;
    text-shadow: 2px 2px 4px rgba(210, 105, 30, 0.3);
    transform: rotate(-1deg);
  }

  .subtitle {
    font-size: 1.3rem;
    color: #a0522d;
    margin: 0;
    font-style: italic;
  }

  .content-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 2rem;
    padding: 1rem 0;
  }

  @media (max-width: 768px) {
    h1 {
      font-size: 2rem;
    }

    .subtitle {
      font-size: 1.1rem;
    }

    .content-grid {
      grid-template-columns: 1fr;
    }
  }
</style>
