# Developer Portfolio Website

A dark-themed portfolio with orange accents and 7-segment display aesthetic, perfect for showcasing your programming projects across multiple languages.

## Features

- 🎨 Dark theme with orange (#ff6b00) accents
- 💻 Matrix rain animated background
- ⌨️ Terminal/hacker aesthetic with monospace fonts
- 🎯 Project filtering by category
- 📊 Interactive skills section with progress bars
- ✨ Smooth animations and transitions
- 🎮 Easter egg (Konami Code)
- 📱 Fully responsive design

## Customization Guide

### 1. Personal Information

**In `index.html`:**

- Line 17-19: Replace `YOUR NAME` with your actual name
- Line 57: Update the subtitle texts in `script.js` (see below)
- Line 288-292: Update About Me text
- Line 310-316: Update interests list
- Line 340: Update email link
- Line 347: Update GitHub link
- Line 354: Update LinkedIn link

### 2. Projects

**To add/edit projects in `index.html` (starting at line 79):**

Each project card has this structure:

```html
<div class="project-card" data-category="game lowlevel">
    <div class="project-image">
        <div class="project-overlay">
            <div class="project-links">
                <a href="YOUR_DEMO_LINK" class="project-link">Demo</a>
                <a href="YOUR_GITHUB_LINK" class="project-link">Code</a>
            </div>
        </div>
    </div>
    <div class="project-info">
        <h3 class="project-title">Your Project Name</h3>
        <p class="project-description">Brief description of your project.</p>
        <div class="project-tech">
            <span class="tech-tag">Language1</span>
            <span class="tech-tag">Language2</span>
        </div>
    </div>
</div>
```

**Categories for `data-category`:**
- `game` - Game Development
- `lowlevel` - Low-Level/Systems Programming
- `web` - Web Development
- `hardware` - Hardware/Embedded Projects

You can combine categories with spaces: `data-category="game web"`

### 3. Skills & Languages

**In `index.html` (lines 176-282):**

Update the project counts and progress bar widths for each language:

```html
<div class="language-item" data-lang="python">
    <div class="lang-header">
        <span class="lang-name">Python</span>
        <span class="project-count">6 projects</span> <!-- Update this -->
    </div>
    <div class="lang-bar">
        <div class="lang-progress" style="width: 88%"></div> <!-- Update this -->
    </div>
</div>
```

The `style="width: 88%"` determines the length of the orange progress bar.

### 4. Typing Effect

**In `script.js` (lines 51-56):**

Update the rotating text that appears below your name:

```javascript
const texts = [
    'Systems Programmer',
    'Game Developer',
    'Hardware Hacker',
    'Full-Stack Developer',
    'Assembly Enthusiast'
];
```

### 5. Colors

**In `styles.css` (lines 4-12):**

```css
:root {
    --bg-primary: #0a0a0a;        /* Main background */
    --bg-secondary: #111111;      /* Section background */
    --bg-tertiary: #1a1a1a;       /* Card background */
    --accent-orange: #ff6b00;     /* Main accent color */
    --text-primary: #ffffff;      /* Main text */
    --text-secondary: #b0b0b0;    /* Secondary text */
}
```

### 6. Add Project Images

To add real images instead of the placeholder:

1. Create an `images` folder next to your HTML file
2. Add your project screenshots/GIFs
3. Replace the `.project-image` div with:

```html
<div class="project-image">
    <img src="images/your-project.png" alt="Project Name" 
         style="width: 100%; height: 100%; object-fit: cover;">
    <div class="project-overlay">
        <!-- ... rest of overlay code ... -->
    </div>
</div>
```

## File Structure

```
portfolio/
│
├── index.html          # Main HTML file
├── styles.css          # All styling
├── script.js           # JavaScript functionality
└── images/            # (Optional) Your project images
    ├── project1.png
    ├── project2.gif
    └── ...
```

## Fonts Used

- **Orbitron** - Headers and titles (7-segment display aesthetic)
- **Share Tech Mono** - Body text and terminal text

These are loaded from Google Fonts automatically.

## Easter Eggs

- **Konami Code**: ↑ ↑ ↓ ↓ ← → ← → B A (activates green "hacker mode")
- **Click particles**: Orange particles burst on every click
- **Console messages**: Open browser console to see welcome message

## Browser Compatibility

- Chrome/Edge: Full support
- Firefox: Full support
- Safari: Full support
- Mobile browsers: Fully responsive

## Tips

1. **Project count**: Keep it accurate by counting how many projects use each language
2. **Progress bars**: Base the width on proficiency or project count (60% = beginner, 90% = advanced)
3. **Descriptions**: Keep project descriptions to 1-2 sentences
4. **Links**: Always include either a demo or code link for each project
5. **Images**: Use 1200x600px images for best results
6. **Loading speed**: Optimize images before uploading (use tools like TinyPNG)

## Deployment

### GitHub Pages:
1. Create a GitHub repository
2. Upload all files (index.html, styles.css, script.js)
3. Go to Settings → Pages
4. Select main branch
5. Your site will be live at `https://yourusername.github.io/repo-name`

### Netlify/Vercel:
1. Drag and drop the folder to their dashboard
2. Instant deployment!

## Future Enhancements

Ideas to make it even better:
- Add a blog section
- Integrate GitHub API to show live repo stats
- Add dark/light mode toggle
- Include downloadable resume
- Add contact form with backend
- Embed playable game demos

---

Built with ❤️ and lots of ☕

For questions or issues, feel free to reach out!
