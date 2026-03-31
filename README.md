# LLM Eval Hub

A consultancy-grade portal for Large Language Model evaluation frameworks, benchmarks, and resources.

## Overview

LLM Eval Hub is a sleek, modern GitHub Pages-ready website that showcases evaluation methodologies, frameworks, benchmarks, and best practices for Large Language Models. Built with pure HTML, CSS, and JavaScript—no build process required.

## Features

- **Dark Mode by Default** with Light Mode Toggle
  - System preference detection
  - User preference saved to localStorage
  - Smooth theme transitions

- **Responsive Design**
  - Mobile-first approach
  - Optimized for all screen sizes (480px - 1440px+)
  - Touch-friendly interface
  - Hamburger menu on mobile

- **Interactive Elements**
  - Scroll-triggered animations
  - Smooth anchor link navigation
  - Active nav link highlighting
  - Back-to-top button
  - Expandable glossary items
  - Benchmark filtering and search

- **Modern Styling**
  - Glassmorphism effects
  - Gradient backgrounds
  - Smooth transitions and animations
  - Custom CSS properties for theming
  - Accessibility-focused design

- **Performance Optimized**
  - No external dependencies
  - Minimal JavaScript
  - CSS animations with GPU acceleration
  - Lazy loading support
  - Responsive images ready

## Quick Start

### 1. Deploy to GitHub Pages

```bash
# Push to your GitHub repository
git push origin main
```

Then enable GitHub Pages in your repository settings pointing to the `main` branch.

### 2. Local Development

Simply open `index.html` in your browser or serve locally:

```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js (http-server)
npx http-server
```

Visit `http://localhost:8000` in your browser.

## File Structure

```
llm-eval-hub/
├── index.html              # Main page
├── css/
│   ├── style.css          # Main stylesheet (~300 lines)
│   ├── responsive.css     # Responsive breakpoints (~150 lines)
│   └── animations.css     # Animation definitions (~100 lines)
├── js/
│   ├── main.js           # Core functionality (~100 lines)
│   ├── theme-toggle.js   # Dark/light mode toggle (~50 lines)
│   └── search.js         # Filter and search features (~80 lines)
└── assets/               # Images, icons, etc.
```

## Customization

### Changing Colors

Edit CSS custom properties in `css/style.css`:

```css
:root {
  --color-accent: #00d4ff;
  --color-primary: #6366f1;
  --color-danger: #ff4757;
  --color-warning: #ffa502;
  --color-success: #2ed573;
}
```

### Updating Content

All content lives in `index.html`. Key sections:
- Navigation links
- Hero section
- Benchmark cards with `data-category` attributes
- Timeline items
- Glossary items
- Footer information

### Customizing URLs

Update all external links in `index.html`:
- Repository links
- Documentation URLs
- Contact information
- Social media profiles

### Adding New Sections

Use the existing grid utilities:

```html
<section class="section">
  <div class="container">
    <h2 class="section-title">New Section</h2>
    <div class="grid-3">
      <!-- Add cards -->
    </div>
  </div>
</section>
```

## Grid Utilities

- `.grid-2` - Two columns
- `.grid-3` - Three columns
- `.grid-4` - Four columns
- `.grid-7` - Seven columns (benchmarks)

## Animation Classes

- `.fade-in` - Fade in on scroll
- `.slide-up` - Slide up on scroll
- `.slide-left` - Slide left on scroll
- `.slide-right` - Slide right on scroll
- `.scale-in` - Scale in on scroll

Add `.stagger-1`, `.stagger-2`, etc. for staggered animations.

## Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari 14+, Chrome Android)

## Responsive Breakpoints

- **1440px+** - Large screens, max-width container
- **1024px - 1439px** - Desktop, 3-column grids
- **768px - 1023px** - Tablet, 2-column grids, hamburger menu
- **480px - 767px** - Small phones, single column
- **< 480px** - Extra small phones, optimized layout

## Performance Tips

1. **Optimize Images**
   - Use WebP format where possible
   - Provide fallback images
   - Lazy load with `loading="lazy"` attribute

2. **Minimize Critical Path**
   - CSS files load in `<head>`
   - Non-critical JS at end of `<body>`
   - Use async/defer for external scripts

3. **Caching**
   - GitHub Pages automatically caches static assets
   - Update cache-busting query params if needed

## Accessibility

- Semantic HTML structure
- ARIA labels where needed
- Keyboard navigation support
- Reduced motion media query respect
- High contrast color combinations
- Focus visible on interactive elements

## Keyboard Shortcuts

- `Ctrl/Cmd + Shift + T` - Toggle theme (if toggle button exists)
- `#section-id` - Anchor navigation with smooth scroll
- `Tab` - Navigate through interactive elements
- `Enter`/`Space` - Activate buttons and glossary items

## JavaScript API

Global functions available via `window.LLMEvalHub`:

```javascript
// Check if element is visible
LLMEvalHub.isElementInViewport(element);

// Add animation to elements
LLMEvalHub.addScrollAnimation('.card', 'fade-in', 100);

// Query parameter helpers
LLMEvalHub.getQueryParameter('filter');
LLMEvalHub.setQueryParameter('filter', 'evaluation');

// Performance utilities
LLMEvalHub.debounce(function, wait);
LLMEvalHub.throttle(function, limit);
```

Theme functions via `window.ThemeToggle`:

```javascript
ThemeToggle.setTheme('light');
ThemeToggle.getCurrentTheme();
ThemeToggle.toggleTheme();
```

Search functions via `window.BenchmarkSearch`:

```javascript
BenchmarkSearch.filterCards(cards, 'data-category', 'framework');
BenchmarkSearch.advancedSearch(cards, criteria);
BenchmarkSearch.resetFilters();
BenchmarkSearch.sortCards(container, 'difficulty');
```

## License

This project is part of the LLM Eval Hub consultancy framework. See the main repository for license details.

## Related

- [LLM Eval Framework Repository](https://github.com/your-org/llm-eval-framework)
- [Documentation](https://docs.example.com)
- [Issues & Feedback](https://github.com/your-org/llm-eval-hub/issues)

## Support

For issues, feedback, or contributions:
1. Open an issue in the GitHub repository
2. Submit a pull request with improvements
3. Check existing documentation and FAQs

---

Built with HTML, CSS, and JavaScript. No build process. Pure web standards.
