# Setup Guide - All Starz Fast Foods Website

This guide will help you set up and customize the All Starz Fast Foods website.

## Quick Start

1. **Clone the repository**:
   ```bash
   git clone https://github.com/NurullahTaha/all-starz-website.git
   cd all-starz-website
   ```

2. **Open the website**:
   - Simply open `index.html` in your web browser
   - No build process required - it's a static website

## Configuration

### EmailJS Setup

The contact form uses EmailJS to send emails. To set it up:

1. Create an account at [EmailJS](https://www.emailjs.com/)
2. Create a new service (Gmail, Outlook, etc.)
3. Create an email template
4. Update the configuration in `assets/js/script.js`:

```javascript
// Replace these with your EmailJS credentials
const emailConfig = {
    serviceID: 'your_service_id',
    templateID: 'your_template_id',
    userID: 'your_user_id'
};
```

### Google Maps API

The location page includes an interactive map. The API key is already configured for the restaurant location, but if you need to change it:

1. Get a Google Maps API key from [Google Cloud Console](https://console.cloud.google.com/)
2. Enable the Maps JavaScript API
3. Update the API key in `index.html`:

```html
<script async defer src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap"></script>
```

## Customization

### Colors and Branding

The website uses CSS custom properties for easy theming. Update these in `assets/css/styles.css`:

```css
:root {
    --primary-gold: #FFF8E7;
    --accent-yellow: #FFD700;
    --accent-orange: #FF9500;
    --accent-red: #8B1538;
    --text-dark: #2C1810;
    --bg-primary: #1A1A1A;
}
```

### Menu Items

To update menu items:

1. Edit the menu sections in `index.html`
2. Add/replace images in `assets/images/`
3. Update prices and descriptions as needed

### Restaurant Information

Update these sections in `index.html`:
- Address in the location section
- Phone number in the footer
- Social media links
- Opening hours

## File Organization

### Assets Structure
```
assets/
├── css/
│   └── styles.css          # All styles
├── js/
│   └── script.js           # All JavaScript
└── images/
    ├── favicon files       # Browser icons
    ├── logo files          # Restaurant logo
    └── menu images         # Food photos
```

### Adding New Images

1. Place images in `assets/images/`
2. Use descriptive filenames
3. Optimize images for web (recommended: under 500KB)
4. Update HTML references to include `assets/images/` path

## Development

### Local Development

1. Open `index.html` directly in browser
2. Make changes to HTML, CSS, or JS files
3. Refresh browser to see changes
4. No build process required

### Testing

Test the website on:
- **Desktop browsers**: Chrome, Firefox, Safari, Edge
- **Mobile devices**: iOS Safari, Chrome Mobile
- **Tablet devices**: iPad, Android tablets

### Common Issues

**Images not loading:**
- Check file paths include `assets/images/`
- Verify image files exist in the images folder
- Check for case-sensitive filename issues

**Contact form not working:**
- Verify EmailJS configuration
- Check browser console for errors
- Ensure EmailJS library is loaded

**Map not displaying:**
- Check Google Maps API key
- Verify API key has proper permissions
- Check browser console for errors

## Deployment

### GitHub Pages (Recommended)

1. Push code to GitHub repository
2. Go to repository Settings > Pages
3. Select "Deploy from a branch"
4. Choose "main" branch and "/ (root)" folder
5. Save and wait for deployment

### Other Hosting Options

The website works on any static hosting provider:
- Netlify
- Vercel
- AWS S3
- Any web server

Simply upload all files maintaining the folder structure.

## Maintenance

### Regular Updates

- Update menu items and prices seasonally
- Refresh food photos regularly
- Update operating hours as needed
- Monitor and respond to form submissions

### Performance

The website is optimized for:
- Fast loading times
- Mobile responsiveness
- Search engine optimization
- Accessibility standards

## Support

For technical support:
- Check the [CONTRIBUTING.md](../CONTRIBUTING.md) file
- Open an issue on GitHub
- Review browser console for error messages

---

**Happy coding! 🍔⭐**