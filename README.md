# Xin Zhou - Professional Website

A professional portfolio website for soprano and voice teacher Xin Zhou, built for GitHub Pages hosting.

## Features

- **Responsive Design**: Works beautifully on desktop, tablet, and mobile devices
- **Modern UI**: Clean, elegant design inspired by professional artist websites
- **Multiple Pages**: 
  - Home
  - About (biography and background)
  - Look (performance photo gallery)
  - Listen (audio/video recordings)
  - Calendar (upcoming performances)
  - Voice Studio (teaching information)
  - Contact (contact form and information)

## Setup for GitHub Pages

### Initial Setup

1. **Create a GitHub Repository**
   - Go to GitHub and create a new repository
   - Name it something like `xinzhou-website` or `xinzhou.github.io` (if you want a custom domain later)

2. **Upload Files**
   - Upload all files from this directory to your GitHub repository
   - Make sure `index.html` is in the root directory

3. **Enable GitHub Pages**
   - Go to your repository on GitHub
   - Click on "Settings"
   - Scroll down to "Pages" in the left sidebar
   - Under "Source", select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click "Save"
   - Your site will be available at `https://yourusername.github.io/repository-name/`

### Custom Domain (Optional)

If you want to use a custom domain (e.g., `xinzhou.com`):

1. Add a file named `CNAME` (no extension) in the root directory with your domain name
2. Configure your domain's DNS settings to point to GitHub Pages
3. GitHub will handle the rest

## Adding Content

### Images

1. Create an `images` folder in the root directory
2. Add your performance photos
3. Name them `performance-1.jpg`, `performance-2.jpg`, etc.
4. The gallery will automatically display them

### Audio/Video Recordings

For the Listen page, you can:

1. **YouTube Videos**: 
   - Upload videos to YouTube
   - Get the embed code
   - Replace the placeholder in `listen.html` with:
   ```html
   <iframe width="560" height="315" src="YOUR_YOUTUBE_URL" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
   ```

2. **SoundCloud Audio**:
   - Upload audio to SoundCloud
   - Get the embed code
   - Add it to `listen.html`

3. **Direct File Hosting**:
   - Add audio/video files to a `media` folder
   - Use HTML5 `<audio>` or `<video>` tags

### Calendar Updates

Edit `calendar.html` to add upcoming performances. Follow the existing format:

```html
<div class="event-item">
    <div class="event-date">
        <span class="event-month">Month</span>
        <span class="event-day">Day</span>
        <span class="event-year">Year</span>
    </div>
    <div class="event-details">
        <h3>Performance Title</h3>
        <p class="event-location">Location</p>
    </div>
</div>
```

### Contact Form

The contact form currently uses a mailto fallback. For full functionality:

1. Use a service like [Formspree](https://formspree.io/) or [Netlify Forms](https://www.netlify.com/products/forms/)
2. Update the form action in `contact.html`
3. Or integrate with a backend service

## File Structure

```
.
├── index.html          # Home page
├── about.html          # About page
├── look.html           # Gallery page
├── listen.html         # Audio/video page
├── calendar.html       # Calendar page
├── voice-studio.html   # Teaching page
├── contact.html        # Contact page
├── styles.css          # Main stylesheet
├── script.js           # JavaScript functionality
├── README.md          # This file
└── images/            # Performance photos (create this folder)
    ├── performance-1.jpg
    ├── performance-2.jpg
    └── ...
```

## Customization

### Colors

Edit the CSS variables in `styles.css`:

```css
:root {
    --primary-color: #2c2c2c;    /* Main text/nav color */
    --secondary-color: #666;      /* Secondary text */
    --accent-color: #8b7355;      /* Accent/hover color */
    --text-color: #333;           /* Body text */
    --light-bg: #f9f9f9;         /* Light backgrounds */
    --white: #ffffff;             /* White */
    --border-color: #e0e0e0;     /* Borders */
    --hover-color: #555;          /* Hover states */
}
```

### Fonts

The site uses Georgia serif font. To change:

1. Update the `font-family` in `styles.css`
2. Or add Google Fonts by including a link in the `<head>` of each HTML file

## Maintenance

- Regularly update the calendar with new performances
- Add new photos to the gallery as they become available
- Update the About page with new achievements or experiences
- Keep contact information current

## Support

For questions or issues, please contact xin22@illinois.edu

## License

This website template is created for Xin Zhou's professional use.

