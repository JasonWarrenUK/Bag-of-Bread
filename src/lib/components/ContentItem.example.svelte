<script lang="ts">
  import SectionCard from "./SectionCard.svelte";
  import ContentItem from "./ContentItem.svelte";
</script>

<!-- Example usage of ContentItem component showing all content types -->

<div class="examples">
  <SectionCard
    icon="📚"
    title="ContentItem Examples"
    strapline="Demonstrating all supported content types"
  >
    <!-- Text Content Example -->
    <ContentItem title="Simple Text Content">
      <p>
        This is a basic example with just text content. You can include multiple
        paragraphs.
      </p>
      <p>
        Each paragraph will be properly styled with appropriate spacing and line
        height for readability.
      </p>
    </ContentItem>

    <!-- Image Example -->
    <ContentItem title="Images">
      <p>Images are automatically styled with proper sizing and shadows:</p>
      <img
        src="https://picsum.photos/600/400"
        alt="Example placeholder image"
      />
      <p>Images will be responsive and include a subtle shadow for depth.</p>
    </ContentItem>

    <!-- Links Example -->
    <ContentItem title="Inline Links" isOpen={true}>
      <p>
        Regular links work great too! Check out <a href="https://svelte.dev"
          >Svelte</a
        >
        or <a href="https://kit.svelte.dev">SvelteKit</a> for more information.
      </p>
      <p>
        Links have a custom style matching the bread theme with hover effects.
      </p>
    </ContentItem>

    <!-- Link Preview Example -->
    <ContentItem title="Link Previews">
      <p>For more prominent links, use the link-preview class:</p>
      <a href="https://svelte.dev" class="link-preview">
        <strong>Svelte - Cybernetically enhanced web apps</strong>
        <p style="margin: 0.5rem 0 0 0; color: #654321;">
          Svelte is a radical new approach to building user interfaces. Whereas
          traditional frameworks do the bulk of their work in the browser,
          Svelte shifts that work into a compile step.
        </p>
      </a>
    </ContentItem>

    <!-- Chart/Data Visualization Example -->
    <ContentItem title="Charts and Visualizations">
      <p>Use the chart-container class for data visualizations:</p>
      <div class="chart-container">
        <div style="text-align: center; padding: 2rem;">
          <strong style="color: #8b4513;">Sample Chart Placeholder</strong>
          <p style="margin: 1rem 0; color: #a0522d;">
            Insert your chart library component here (Chart.js, D3, etc.)
          </p>
          <div
            style="height: 200px; background: linear-gradient(to top, #f5deb3, #fff); border-radius: 8px; display: flex; align-items: flex-end; justify-content: space-around; padding: 1rem;"
          >
            <div
              style="width: 40px; height: 60%; background: #d2691e; border-radius: 4px 4px 0 0;"
            ></div>
            <div
              style="width: 40px; height: 85%; background: #d2691e; border-radius: 4px 4px 0 0;"
            ></div>
            <div
              style="width: 40px; height: 45%; background: #d2691e; border-radius: 4px 4px 0 0;"
            ></div>
            <div
              style="width: 40px; height: 70%; background: #d2691e; border-radius: 4px 4px 0 0;"
            ></div>
          </div>
        </div>
      </div>
    </ContentItem>

    <!-- Mixed Content Example -->
    <ContentItem title="Mixed Content">
      <p>You can combine multiple content types in one item:</p>
      <img src="https://picsum.photos/400/300" alt="Another example" />
      <p>
        Add descriptive text alongside images, and include
        <a href="https://example.com">relevant links</a> within the content.
      </p>
      <a href="https://example.com" class="link-preview">
        <strong>Related Resource</strong>
        <p style="margin: 0.5rem 0 0 0; color: #654321;">
          Additional information and resources can be highlighted with link
          previews.
        </p>
      </a>
    </ContentItem>

    <!-- Initially Open Example -->
    <ContentItem title="Pre-opened State" isOpen={true}>
      <p>
        This ContentItem was initialized with <code
          >isOpen=&#123;true&#125;</code
        >, so it starts in the open state.
      </p>
      <p>
        Users can still close it by clicking the header, and the state will be
        managed internally.
      </p>
    </ContentItem>
  </SectionCard>
</div>

<style>
  .examples {
    max-width: 800px;
    margin: 0 auto;
    padding: 2rem 0;
  }

  code {
    background: rgba(139, 69, 19, 0.1);
    padding: 0.2em 0.4em;
    border-radius: 3px;
    font-family: "Monaco", "Courier New", monospace;
    font-size: 0.9em;
    color: #8b4513;
  }
</style>
