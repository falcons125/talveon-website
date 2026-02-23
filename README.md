# Talveon Website

Professional business website for Talveon.com

## Files Included

- `index.html` - Homepage
- `about.html` - About page
- `services.html` - Services page
- `contact.html` - Contact page with Netlify form
- `404.html` - Custom 404 error page
- `styles.css` - Complete stylesheet
- `robots.txt` - SEO configuration
- `sitemap.xml` - Sitemap for search engines

## Features

✅ Fully responsive design (mobile, tablet, desktop)
✅ Professional blue color scheme
✅ Contact form integrated with Netlify Forms
✅ SEO-optimized with meta tags
✅ Fast loading and clean code
✅ Cross-browser compatible

## How to Deploy to Netlify

### Method 1: Drag & Drop (Easiest)

1. **Zip this folder** (or select all files)
2. Go to [app.netlify.com](https://app.netlify.com)
3. Click "Add new site" → "Deploy manually"
4. Drag the entire folder into the deploy zone
5. Wait for deployment to complete
6. Your site will be live at a temporary URL

### Method 2: Netlify CLI

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Deploy
cd talveon-website
netlify deploy --prod
```

## Connecting Your Domain

After deploying to Netlify:

1. Go to Site Settings → Domain Management
2. Click "Add a domain"
3. Enter: `talveon.com`
4. Follow the DNS configuration instructions in the setup guide

## Customization

### Update Content

Edit the HTML files to customize:
- Company name and description
- Services offered
- Contact information
- Any text content

### Change Colors

Edit `styles.css` and modify the CSS variables at the top:

```css
:root {
    --primary-color: #2563eb;    /* Main blue color */
    --secondary-color: #1e40af;  /* Darker blue */
    --text-dark: #1f2937;        /* Dark text */
    --text-light: #6b7280;       /* Light text */
}
```

### Add Google Analytics

Add this code to the `<head>` section of each HTML file:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR-GA-ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR-GA-ID');
</script>
```

## Contact Form

The contact form is configured to work with Netlify Forms automatically. Form submissions will appear in your Netlify dashboard under:

**Site Settings → Forms**

You can set up email notifications for new form submissions.

## Support

For issues or questions:
- Netlify Documentation: https://docs.netlify.com
- Netlify Support: https://answers.netlify.com

## License

All rights reserved © 2026 Talveon
