# BLOOM Landing Page

A distinctive, production-grade landing page for Bianca Venturotti's webinar on brand strategy and positioning.

## 🎨 Design Philosophy

This landing page follows the **Front-End Agent** principles, avoiding generic AI aesthetics through:

- **Distinctive Typography**: Cormorant Garamond (display) + DM Sans (body)
- **Sophisticated Color Palette**: Editorial earth tones (cream, sage, terracotta, gold)
- **Extensive Animations**: Staggered entrances, parallax effects, micro-interactions
- **Editorial Luxury Aesthetic**: Magazine-inspired layout with generous negative space

## 📁 Project Structure

```
lp-bloom claude/
├── index.html          # Main HTML structure
├── styles.css          # Complete styling with animations
├── script.js           # Interactive features and form handling
├── resources/          # Images and assets
│   ├── bianca-hero.png
│   └── bianca-bio.jpg
└── README.md           # This file
```

## 🚀 Quick Start

### Local Development

Simply open `index.html` in your browser:

```bash
open index.html
```

Or use a local server for better development experience:

```bash
# Using Python 3
python3 -m http.server 8000

# Using Node.js (if you have http-server installed)
npx http-server -p 8000
```

Then visit: `http://localhost:8000`

## ✨ Features

### Interactive Elements
- ✅ **FAQ Accordion** — Smooth expand/collapse with rotation animation
- ✅ **Hover Effects** — Cards lift and show gradient borders
- ✅ **Smooth Scroll** — Anchor links navigate smoothly
- ✅ **Form Validation** — Brazilian phone formatting `(XX) XXXXX-XXXX`
- ✅ **Scroll Animations** — Intersection Observer for entrance effects
- ✅ **Custom Cursor** — Desktop-only enhanced cursor (optional)

### Responsive Design
- Mobile-first approach
- Breakpoints: 968px (tablet) and 640px (mobile)
- Grid layouts adapt to single column
- Optimized typography and spacing

## 📝 Customization

### Update Event Details

Edit `index.html` lines 38-41 to add actual date and time:

```html
<div class="detail__item">
    <span class="detail__icon">📅</span>
    <span class="detail__text">Data: <strong>15 de Fevereiro, 2026</strong></span>
</div>
```

### Configure Form Submission

Edit `script.js` around line 24 to connect to your backend:

```javascript
registrationForm.addEventListener('submit', function(e) {
    e.preventDefault();
    
    const formData = {
        name: document.getElementById('name').value,
        email: document.getElementById('email').value,
        phone: document.getElementById('phone').value,
        company: document.getElementById('company').value,
        role: document.getElementById('role').value
    };
    
    // Replace with your API endpoint
    fetch('https://your-api.com/register', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(formData)
    })
    .then(response => response.json())
    .then(data => {
        alert('Inscrição realizada com sucesso!');
        registrationForm.reset();
    })
    .catch(error => {
        console.error('Error:', error);
        alert('Erro ao processar inscrição. Tente novamente.');
    });
});
```

### Modify Colors

Edit CSS variables in `styles.css` (lines 1-10):

```css
:root {
    --color-cream: #FAF7F2;
    --color-charcoal: #1A1A1A;
    --color-sage: #8B9D83;
    --color-terracotta: #D4735E;
    --color-gold: #C9A961;
    /* ... */
}
```

## 🌐 Deployment

### Option 1: Static Hosting (Recommended)

Deploy to platforms like:

- **Vercel**: `vercel --prod`
- **Netlify**: Drag and drop the folder
- **GitHub Pages**: Push to `gh-pages` branch
- **AWS S3**: Upload to S3 bucket with static hosting

### Option 2: Traditional Web Hosting

Upload all files via FTP to your web host:
- `index.html`
- `styles.css`
- `script.js`
- `resources/` folder

## 📊 Analytics Integration

Add Google Analytics before closing `</head>` tag:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🔧 Technical Details

### Dependencies
- **Google Fonts**: Cormorant Garamond, DM Sans
- **No JavaScript frameworks** — Vanilla JS only
- **No CSS frameworks** — Custom CSS with variables

### Browser Support
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

### Performance
- Estimated load time: < 2 seconds
- Optimized animations (CSS-only where possible)
- Lazy loading for images
- Minimal external dependencies

## 📱 Testing Checklist

Before going live:

- [ ] Update event date and time
- [ ] Configure form backend endpoint
- [ ] Test on mobile devices (iOS and Android)
- [ ] Verify all images load correctly
- [ ] Test form submission
- [ ] Add analytics tracking
- [ ] Check all links work
- [ ] Test FAQ accordion
- [ ] Verify smooth scroll on all CTAs
- [ ] Check responsive breakpoints

## 🎯 Conversion Optimization

The page is structured for maximum conversion:

1. **Hero** — Immediate impact and identification
2. **Identification** — Filter qualified leads
3. **Value** — Justify time investment
4. **Authority** — Build credibility
5. **After** — Present upsells without pressure
6. **FAQ** — Remove objections
7. **CTA Final** — Convert with urgency

## 📞 Support

For questions or customization help, refer to:
- [walkthrough.md](../brain/383964c8-27ac-4266-a40b-3b9ef38eba80/walkthrough.md) — Detailed implementation guide
- [Landing Page Content.txt](Landing%20Page%20Content.txt) — Original content strategy

## 📄 License

All rights reserved © Bianca Venturotti

---

**Built with the Front-End Agent** — Distinctive design, production-grade code, zero generic aesthetics.

🌸 **BLOOM is ready to convert.**
