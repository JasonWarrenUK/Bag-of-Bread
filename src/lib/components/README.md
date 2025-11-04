# Components Documentation

This directory contains reusable Svelte components for the Bag of Bread application.

## SectionCard

A semantic section card component that displays a header with an icon, title, and strapline.

### Props

- `icon: string` - An emoji or character to display as the card icon
- `title: string` - The main heading for the section
- `strapline: string` - A descriptive subtitle/tagline

### Usage

```svelte
<SectionCard
  icon="🥖"
  title="Fresh Content"
  strapline="Hot out of the oven and ready to consume"
>
  <!-- Optional content goes here -->
</SectionCard>
```

### Features

- Semantic `<section>` element as the root
- Semantic `<header>` for the card header
- Icon and title displayed inline in the section title
- Hover effects with rotation and elevation
- Responsive design
- Accepts slotted content for the card body

## ContentItem

A toggleable accordion-style component for displaying collapsible content within sections.

### Props

- `title: string` - The heading displayed in the toggle button
- `isOpen: boolean = false` - Initial open/closed state (optional, defaults to closed)

### Usage

```svelte
<ContentItem title="Latest Updates">
  <p>Check out our newest additions to the collection. Fresh daily!</p>
</ContentItem>

<ContentItem title="Pre-opened Item" isOpen={true}>
  <p>This item starts in the open state.</p>
</ContentItem>
```

### Features

- Starts with semantic `<h3>` element
- Fully keyboard accessible (button-based toggle)
- Click or press Enter to toggle open/closed
- Smooth slide-down animation when opening
- Visual indicator (▶ when closed, ▼ when open)
- Styled to support various content types:
  - Text paragraphs
  - Images (with automatic styling)
  - Links (with custom styling)
  - Link previews (use `.link-preview` class)
  - Charts (use `.chart-container` class)

### Content Types Examples

**Text:**
```svelte
<ContentItem title="Information">
  <p>Regular paragraph text.</p>
  <p>Multiple paragraphs are supported.</p>
</ContentItem>
```

**Images:**
```svelte
<ContentItem title="Visual Content">
  <img src="/path/to/image.jpg" alt="Description" />
  <p>Caption text below the image.</p>
</ContentItem>
```

**Links:**
```svelte
<ContentItem title="References">
  <p>Check out <a href="https://example.com">this resource</a>.</p>
</ContentItem>
```

**Link Previews:**
```svelte
<ContentItem title="Resources">
  <a href="https://example.com" class="link-preview">
    <strong>Article Title</strong>
    <p>Preview description of the linked content...</p>
  </a>
</ContentItem>
```

**Charts:**
```svelte
<ContentItem title="Data Visualization">
  <div class="chart-container">
    <!-- Chart component or visualization goes here -->
  </div>
</ContentItem>
```

## Design Principles

- **Semantic HTML**: Uses appropriate semantic elements (`<section>`, `<header>`, `<article>`, `<button>`)
- **Accessibility**: Keyboard navigable, proper ARIA attributes, focus states
- **Responsive**: Works on mobile and desktop
- **Themeable**: Consistent color scheme with the bread theme
- **Smooth interactions**: Transitions and animations for better UX