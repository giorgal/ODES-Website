# ODES Website

Official website for **ODES** (Orbital Dynamics and Engineering Solutions) - a space technology company focused on mission validation and simulation platforms for the New Space era.

## 🚀 About ODES

ODES provides comprehensive validation platforms for satellite missions, addressing the critical challenge of satellite failures in orbit. The company offers simulation, validation, hardware-in-the-loop testing, and mission analytics solutions.

## 🌐 Website Structure

### Main Pages
- **index.html** - Homepage with company overview, capabilities, services, projects, team, and contact
- **philosophy.html** - Company philosophy and approach to space mission validation
- **insights.html** - Blog/articles section with industry insights and technical content
- **article-template.html** - Template for individual article pages

### Key Sections (index.html)
1. **Hero** - Brand positioning: "Validation Beyond Boundaries"
2. **Why ODES** - Problem statement and solution overview
3. **Capabilities** - Core technical capabilities and platform features
4. **Services** - Service offerings and value propositions
5. **Projects** - Featured missions (HSD, ERMIS, HELEO) and partnerships
6. **Team** - Company founders and key personnel
7. **Contact** - Contact forms and information

## 🛠 Technology Stack

- **HTML5/CSS3** - Core structure and styling
- **Vanilla JavaScript** - Interactive functionality
- **Google Fonts** - Space Grotesk typography
- **Formspree** - Contact form backend
- **No build tools required** - Direct browser deployment

### External Dependencies (CDN)
- Google Fonts (Space Grotesk)
- Formspree form handling

## 📁 Project Structure

```
ODES-Website/
├── index.html                      # Main homepage
├── philosophy.html                 # Philosophy page
├── insights.html                   # Insights/blog listing page
├── article-template.html           # Template for article pages
├── odes-RGB-reverse.png           # Company logo
├── background.jpg                  # Background image
├── favicon.png                     # Site favicon
├── gradient-banner-preview.png    # Banner asset
├── video1.mp4                      # Demo video 1
├── video2.mp4                      # Demo video 2
├── insights/
│   └── articles/
│       └── articles.js            # Article data and metadata
├── missions/                       # Mission-related assets
├── CLAUDE.md                       # AI assistant guidance
├── ASSETS-NEEDED.md               # Asset requirements documentation
└── README.md                       # This file
```

## 🎨 Design System

### Color Palette
- **Primary Purple**: `#BD4FCF` (rgb(189, 79, 207))
- **Secondary Purple**: `#667eea`, `#764ba2`
- **Background Dark**: `#0a0a0a`, `#1a1a1a`
- **Accent Coral**: `#ff6b6b`, `#ee5a6f`
- **Text**: White (`#ffffff`) with varying opacity
- **Borders**: `rgba(255, 255, 255, 0.1)`

### Typography
- **Font Family**: Space Grotesk (Google Fonts)
- **Weights**: 400 (Regular), 500 (Medium), 600 (Semi-Bold), 700 (Bold)

### Animations
- Fade-in animations on scroll
- Smooth scrolling between sections
- Hover effects on cards and buttons
- Video autoplay on scroll into view
- Interactive navigation highlighting

## 🚀 Development

### Local Development
```bash
# Option 1: Using Python's built-in server
python3 -m http.server 8000

# Option 2: Using Node.js http-server (if installed)
npx http-server -p 8000

# Then open: http://localhost:8000/index.html
```

### File Editing
No build process required - simply edit HTML files directly and refresh the browser.

### Testing Checklist
- [ ] Responsive design (mobile, tablet, desktop)
- [ ] Smooth scrolling between sections
- [ ] Navigation highlighting on scroll
- [ ] Contact form submissions
- [ ] Video autoplay behavior
- [ ] Cross-browser compatibility (Chrome, Firefox, Safari, Edge)
- [ ] Performance optimization (image/video loading)

## 📝 Content Management

### Adding New Articles (Insights)
1. Edit `/insights/articles/articles.js` to add article metadata
2. Create new HTML file using `article-template.html` as reference
3. Update `insights.html` if manual article list management is needed

### Updating Contact Information
- Email: `info@odes-space.com`
- Contact forms use Formspree endpoints (configured in HTML)
- Three form types: General Contact, Demo Request, Info Request

### Modifying Team Information
Team members are hardcoded in `index.html`. Edit the Team section to update:
- Names and titles
- Photos (stored in root or specify path)
- Descriptions and expertise

## 🔧 Key Features

### Interactive Elements
- **Sticky Navigation** - Fixed header with scroll effects
- **Splash Screen** - Initial loading animation (skippable)
- **Modal Contact Forms** - Three different contact form types
- **Mobile Menu** - Responsive hamburger menu
- **Smooth Scrolling** - Animated transitions between sections
- **Video Demos** - Auto-playing demo videos on scroll
- **CAPTCHA Validation** - Simple math-based spam prevention

### Form Types
1. **General Contact** (`#contactModal`) - For general inquiries
2. **Demo Request** (`#demoModal`) - Request product demonstrations
3. **Info Request** (`#infoModal`) - Request additional information

### Navigation Features
- Logo click scrolls to top
- Automatic section highlighting on scroll
- Mobile-responsive menu
- Smooth anchor link scrolling

## 🌍 Deployment

### GitHub Pages
```bash
# Push to main branch
git push origin main

# Configure GitHub Pages in repository settings
# Select branch: main
# Folder: / (root)
```

### Custom Domain
Update DNS settings to point to GitHub Pages:
```
A Record: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
CNAME Record: [your-username].github.io
```

### Traditional Web Hosting
Simply upload all files to your web server root directory. Ensure:
- `index.html` is the default document
- All asset files (images, videos) are uploaded
- File permissions are set correctly

## 📧 Contact Forms

All forms use Formspree backend:
- Contact Form: `https://formspree.io/f/xdkppwln`
- Demo Form: `https://formspree.io/f/xpwaoavy`
- Info Form: `https://formspree.io/f/xnnqnorz`

Update these endpoints in the HTML if you need to change form handling.

## 🔒 Security Notes

- CAPTCHA implemented for spam prevention (simple math challenge)
- Form validation on client-side and Formspree server-side
- No sensitive data stored client-side
- External form handling via Formspree (third-party service)

## 📊 Analytics

Currently no analytics tracking is implemented. To add:
- Google Analytics (add tracking code to `<head>`)
- Meta Pixel (add pixel code to `<head>`)
- Custom event tracking as needed

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

© 2025 ODES. All rights reserved.

## 📞 Support

For technical issues or questions:
- Email: info@odes-space.com
- Website: [ODES Space](https://odes-space.com)

---

**Note**: This website uses no backend framework and minimal external dependencies for maximum portability and ease of deployment.
