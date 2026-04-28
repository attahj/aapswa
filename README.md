# Afghan Community of Puget Sound - Community Center Website

A modern, responsive website for the Afghan Association of Puget Sound's community center fundraising campaign, optimized for GitHub Pages hosting.

## 📁 File Structure

```
.
├── index.html          # Main website file
├── js/
│   └── script.js       # JavaScript for interactivity
├── README.md           # This file
└── .nojekyll          # Tells GitHub to serve static files directly
```

## ✨ Features

- **Fully Responsive Design** - Works perfectly on mobile, tablet, and desktop
- **Modern, Professional Look** - Built with Tailwind CSS for clean styling
- **No Build Required** - Pure HTML, CSS, and JavaScript
- **Fast Loading** - Uses CDN for styles and icons
- **Accessible** - Semantic HTML and ARIA labels
- **SEO Optimized** - Meta tags and structured content

## 🎨 Sections Included

1. **Navigation Header** - Fixed header with mobile menu
2. **Hero Section** - Eye-catching banner with call-to-action buttons
3. **About Section** - Organization info, stats, and core values
4. **Project Section** - Community center features and vision
5. **Progress Section** - Fundraising progress tracker
6. **Donation Section** - Multiple donation methods and options
7. **Contact Section** - Contact form and information
8. **Footer** - Links, social media, and newsletter signup

## 🔧 Customization

### Update Organization Name, Contact Info, and Links

Edit `index.html` and replace:
- Organization name and descriptions
- Contact email and phone number
- Social media links in the footer
- Donation amounts and methods

### Change Colors

The color scheme uses Tailwind CSS classes. To change from amber/orange to another color:
1. Replace `amber-600`, `amber-400`, `amber-50`, etc. with other Tailwind colors
2. Options: `blue`, `green`, `purple`, `red`, `pink`, etc.

### Add Your Own Images

Replace the image URL in the Hero section background:
```html
backgroundImage: 'url(YOUR_IMAGE_URL_HERE)'
```

## 📧 Contact Form

The contact form currently shows an alert. To make it functional:
1. Use a service like [Formspree](https://formspree.io) or [EmailJS](https://www.emailjs.com)
2. Update the form submission handler in `js/script.js`

## ✅ Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📱 Mobile Optimization

- Responsive navigation with mobile hamburger menu
- Touch-friendly buttons and links
- Optimized images for all screen sizes
- Readable text on all devices

## 🔒 Privacy & Security

- No data collection by default
- All contact form submissions require custom backend setup
- HTTPS automatically enabled on GitHub Pages

## 📄 License

This website template is provided as-is for use by Afghan Association of Puget Sound and similar community organizations.

---

**Last Updated:** April 2026
**Version:** 1.0
