<script lang="ts">
  import SectionCard from "$lib/components/SectionCard.svelte";
  import ContentItem from "$lib/components/ContentItem.svelte";

  let title = "Welcome to Bag of Bread!";
</script>

<svelte:head>
  <title>Bag of Bread • Crumbs and Nuggets</title>
  <meta
    name="description"
    content="A collection of resources and information, baked to perfection"
  />
</svelte:head>

<div class="home">
  <div class="hero">
    <h1>{title}</h1>
    <p class="subtitle">The discerning loaf's favoured source for delicious crumbs of wisdom</p>
  </div>

  <div class="content-grid">
    <SectionCard <!-- News, updates, time-relevant -->
      icon="🥖"
      title="Fresh News"
      strapline="Hot out of the oven and ready to consume"
    >
      <ContentItem title="Claude for Sheets">
        <p>Anthropic's Claude AI is now available as a Google Sheets extension, bringing powerful AI capabilities directly into your spreadsheets. Perfect for data analysis, content generation, and cost calculations without writing any code!</p>
        <p><a href="https://www.anthropic.com/news/claude-for-sheets" target="_blank" rel="noopener">Read the announcement from Anthropic</a></p>
        <img src="https://www.anthropic.com/_next/image?url=https%3A%2F%2Fwww-cdn.anthropic.com%2Fimages%2F4zrzovbb%2Fwebsite%2Fd25d09d7c21adc56faea8a07e847bd06ce2b27f6-3840x2160.png&w=3840&q=75" alt="Claude for Sheets interface showing AI integration in spreadsheets" />
        <p>This tool is ideal for beginners because it requires no programming knowledge - just type natural language prompts directly into spreadsheet cells to analyze data, generate content, or perform cost analysis calculations.</p>
      </ContentItem>
    </SectionCard>

    <SectionCard <!-- Tutorials, guides, tools, explainers -->
      icon="🥐"
      title="Flaky Resources"
      strapline="Layered with knowledge and buttery smooth"
    >
      <ContentItem title="Using Claude for Game Design">
        <p>Claude can be an incredible creative partner for both digital and tabletop game design. This beginner-friendly guide shows you how to use Claude to brainstorm mechanics, balance gameplay, write dialogue, and even generate rule systems for board games.</p>
        <p>
          <a href="https://docs.anthropic.com/en/docs/about-claude/use-case-guides/game-development" target="_blank" rel="noopener">Explore Claude's Game Development Guide</a>
        </p>
        <p>Perfect for game designers who want to prototype faster without needing to write complex code. Simply describe what you want to create, and Claude can help you iterate on ideas, generate content, and even create simple game logic in Python that you can copy and paste.</p>
        <div class="link-preview">
          <strong>Related:</strong>
          <a href="https://www.anthropic.com/research" target="_blank" rel="noopener">Learn more about Claude's capabilities</a>
        </div>
      </ContentItem>

      <ContentItem title="Claude API for Document Processing">
        <p>Working with large text documents? The Claude API can summarize reports, extract key information, answer questions about your documents, and even help you organize content - all without needing programming experience if you use tools like Claude.ai's web interface.</p>
        <p>
          <a href="https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/long-context-tips" target="_blank" rel="noopener">Read the guide on working with long documents in Claude</a>
        </p>
        <img src="https://www.anthropic.com/_next/image?url=https%3A%2F%2Fwww-cdn.anthropic.com%2Fimages%2F4zrzovbb%2Fwebsite%2Fc9c97044e5c0384b7fde7063c005ac9ef7fd55bf-3840x2160.png&w=3840&q=75" alt="Claude processing long documents" />
        <p>Claude can handle documents up to hundreds of pages long, making it ideal for research, content analysis, and documentation review. You can paste your text directly into the chat interface and ask questions in plain English.</p>
      </ContentItem>
      <ContentItem title="Prompt Library: Practical Examples for Beginners">
        <p>Anthropic's official prompt library includes ready-to-use examples for game design, spreadsheet analysis, and document processing. Each prompt includes clear explanations and can be copied directly into Claude without any coding required.</p>
        <p><a href="https://docs.anthropic.com/en/prompt-library/library" target="_blank" rel="noopener">Browse the complete prompt library</a></p>
        <div class="link-preview">
          <strong>Featured examples include:</strong> Game narrative generation, CSV data analysis, cost-benefit analysis templates, and document summarization workflows
        </div>
      </ContentItem>
    </SectionCard>

    <SectionCard <!-- All other content -->
      icon="🥯"
      title="Doughy Linklumps"
      strapline="Everything you knead to know"
    >
      <ContentItem title="Claude's Token Counter & Cost Calculator">
        <p>Before you start using Claude's API, understand how much it will cost! This interactive tool helps you estimate costs by showing you how many tokens your text uses. No programming knowledge needed - just paste your text and see the results.</p>
        <p><a href="https://docs.anthropic.com/en/docs/resources/token-counting" target="_blank" rel="noopener">Visit the token counting documentation</a></p>
        <p>This is especially useful if you're planning to process spreadsheets, game dialogue, or large documents and want to keep your costs predictable. The documentation includes clear pricing tables and examples in plain English.</p>
        <div class="link-preview">
          <strong>Bonus:</strong>
          <a href="https://console.anthropic.com" target="_blank" rel="noopener">Claude Console</a> - Try Claude directly in your browser with $5 in free credits to experiment
        </div>
      </ContentItem>
      <ContentItem title="Community Cookbook: Real-World Applications">
        <p>The Anthropic Cookbook repository features complete, beginner-friendly tutorials for using Claude with Excel files, game content generation, and cost analysis. Each tutorial includes step-by-step instructions and Python code that you can run with minimal setup.</p>
        <p><a href="https://github.com/anthropics/anthropic-cookbook" target="_blank" rel="noopener">Explore the Claude Cookbook on GitHub</a></p>
        <img src="https://opengraph.githubassets.com/1/anthropics/anthropic-cookbook" alt="Anthropic Cookbook repository preview" />
        <p>While the examples use Python, many are simple enough for beginners to follow along with just a basic understanding of the syntax. Topics include working with spreadsheets, analyzing game balance, and processing documents at scale.</p>
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
