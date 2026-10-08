# Advanced Customization Guide

## Color Palette Generator

Use these websites to generate color palettes:
- https://coolors.co/
- https://color.adobe.com/
- https://www.color-hex.com/

## Google Fonts Integration

All Google Fonts are automatically loaded. Popular combinations:

### Elegant & Modern
**Title Font:** Playfair Display
**Body Font:** Open Sans
```css
font-family: 'Playfair Display', serif;
font-family: 'Open Sans', sans-serif;
```

### Classic & Sophisticated
**Title Font:** Merriweather
**Body Font:** Lato
```css
font-family: 'Merriweather', serif;
font-family: 'Lato', sans-serif;
```

### Minimal & Tech
**Title Font:** Montserrat
**Body Font:** Roboto
```css
font-family: 'Montserrat', sans-serif;
font-family: 'Roboto', sans-serif;
```

### Friendly & Modern
**Title Font:** Raleway
**Body Font:** Nunito
```css
font-family: 'Raleway', sans-serif;
font-family: 'Nunito', sans-serif;
```

## Color Schemes

### Dark Mode (Dark Background)
```css
body {
    background-color: #1a1a1a;
    color: #f0f0f0;
}

.post {
    background: #2d2d2d;
    color: #f0f0f0;
}
```

### Light & Airy
```css
body {
    background-color: #ffffff;
    color: #333;
}

header {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

### Professional Blue
```css
header {
    background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
}

nav {
    border-bottom: 2px solid #1e3c72;
}
```

### Warm & Inviting
```css
header {
    background: linear-gradient(135deg, #f77f00 0%, #fcbf49 100%);
}
```

### Nature Green
```css
header {
    background: linear-gradient(135deg, #2d6a4f 0%, #40916c 100%);
}
```

## CSS Selectors for Customization

### Typography
```css
/* All links */
a {
    color: #667eea;
}

/* Link hover */
a:hover {
    color: #764ba2;
}

/* Headings */
h1, h2, h3 {
    color: #1a1a1a;
}

/* Post title */
.post-title {
    font-size: 1.8rem;
}
```

### Spacing
```css
/* Post padding */
.post {
    padding: 2.5rem;  /* Increase for more space */
}

/* Section padding */
main {
    padding: 3rem 0;  /* Increase for more vertical space */
}
```

### Borders & Shadows
```css
/* Post box shadow */
.post {
    box-shadow: 0 2px 8px rgba(0,0,0,0.08);
}

/* Remove shadow (make it subtle) */
.post {
    box-shadow: none;
    border: 1px solid #e0e0e0;
}

/* Increase shadow (more pronounced) */
.post {
    box-shadow: 0 10px 30px rgba(0,0,0,0.15);
}
```

### Border Radius (Roundness)
```css
/* More rounded corners */
.post {
    border-radius: 16px;  /* Increase value for rounder corners */
}

/* Square corners */
.post {
    border-radius: 0;
}
```

## Quick Customization Snippets

### Change Post Box Style to Card with Border
Replace:
```css
.post {
    background: white;
    padding: 2.5rem;
    margin-bottom: 2rem;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.08);
}
```

With:
```css
.post {
    background: white;
    padding: 2.5rem;
    margin-bottom: 2rem;
    border-radius: 0;
    box-shadow: none;
    border-left: 4px solid #667eea;
    border-bottom: 1px solid #e0e0e0;
}
```

### Monochrome Theme
Replace all gradient colors with single color:
```css
/* Before */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* After - Single gray */
background: #555;

/* After - Single blue */
background: #2c3e50;
```

### Minimal Theme (Remove Shadows & Borders)
```css
.post {
    box-shadow: none;
    border: none;
    border-top: 1px solid #e0e0e0;
    border-radius: 0;
}

.categories-section {
    box-shadow: none;
    border: 1px solid #e0e0e0;
}
```

### Bold & Colorful Categories
```css
.category-item {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 1.5rem;  /* Increase padding */
    font-size: 1.1rem;  /* Larger text */
    font-weight: bold;
}
```

## Mobile Customization

### Increase Mobile Font Size
Find:
```css
@media (max-width: 768px) {
    header h1 {
        font-size: 1.8rem;
    }
}
```

Change to:
```css
@media (max-width: 768px) {
    header h1 {
        font-size: 2.2rem;
    }
}
```

### Stack Navigation Vertically on Mobile
```css
@media (max-width: 768px) {
    nav .container {
        flex-direction: column;
        gap: 1rem;
    }
}
```

## Advanced: Custom CSS Classes

Add these snippets anywhere in the `<b:skin>` section to create custom styles:

### Highlighted Box for Important Content
```css
.highlight-box {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 1.5rem;
    border-radius: 8px;
    margin: 1.5rem 0;
}
```

### Styled Quote
```css
.styled-quote {
    border-left: 4px solid #667eea;
    padding-left: 1.5rem;
    font-style: italic;
    color: #666;
    margin: 1.5rem 0;
}
```

### Info Box
```css
.info-box {
    background: #f0f0f0;
    border-radius: 8px;
    padding: 1.5rem;
    margin: 1.5rem 0;
    border-left: 4px solid #667eea;
}
```

## Testing Your Changes

1. **Always make one change at a time**
2. **Take a screenshot** before changing
3. **Save and refresh** (Ctrl+F5 to clear cache)
4. **Wait 5-10 seconds** for Blogger to process
5. **Check on mobile** using DevTools (F12)

## Common Issues & Solutions

| Issue | Solution |
|-------|----------|
| Colors not changing | Clear cache (Ctrl+Shift+Delete), wait 10 minutes |
| Fonts not loading | Check Google Fonts are spelled correctly |
| Mobile looks broken | Check media queries in CSS |
| Links not working | Verify full URLs, use https:// |
| Posts too wide | Decrease `max-width` value |
| Text too small | Increase `font-size` values |

## Performance Tips

1. **Minimize custom fonts** - Using 2-3 fonts is optimal
2. **Optimize images** - Compress before uploading
3. **Use simple gradients** - Avoid too many color transitions
4. **Limit animations** - Keep transitions to 0.3s-0.5s

---

**Need help? Check the README.md or contact through your blog's contact page.**