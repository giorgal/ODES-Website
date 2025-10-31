# Assets Needed for ODES Website

## 🎯 High Priority (Essential for Launch)

### 1. Social Media Card Image
- **File:** `odes-social-card.png`
- **Dimensions:** 1200x630px
- **Purpose:** Displays when website is shared on LinkedIn, Twitter, Facebook
- **Content Suggestion:** ODES logo + tagline + gradient background
- **Format:** PNG or JPG

### 2. Actual Screenshots/Photos

#### Operational Simulator Image
- **Location:** Replaces placeholder at line 522-532 in index.html
- **Dimensions:** 16:9 aspect ratio (e.g., 1920x1080px)
- **Content:** Screenshot of ODES simulator interface in action
- **Format:** PNG, JPG, or WebP

#### External Facility Integration Image
- **Location:** Replaces placeholder at line 604-614 in index.html
- **Dimensions:** 16:9 aspect ratio (e.g., 1920x1080px)
- **Content:** Photo of hardware integration, testing facility, or infrastructure
- **Format:** PNG, JPG, or WebP

### 3. Testimonials Content
- **Location:** Lines 775-789 in index.html
- **Need:** 3 customer testimonials
- **Each testimonial should include:**
  - Quote (2-3 sentences about their experience with ODES)
  - Customer name
  - Job title
  - Company name
- **Example format:**
  ```
  Quote: "ODES reduced our validation cycle by 40% while improving test coverage. Their platform integrated seamlessly with our existing tools."
  Name: "Dr. Sarah Chen"
  Role: "Chief Engineer, Stellar Dynamics"
  ```

## 🌟 Recommended (Enhances Credibility)

### 4. Team Photos
- **Location:** Team section (lines 800-832)
- **Need:** Professional headshots for:
  - Giorgos Galanos (CEO)
  - Orestis Ousoultzoglou (CTO)
  - Romanos Voulgarakis (CSO)
  - Nikos Livanos (Business Advisor)
- **Dimensions:** Square format (e.g., 400x400px)
- **Style:** Professional, consistent background/lighting
- **Format:** PNG or JPG

### 5. Customer/Partner Logos
- **Purpose:** "Trusted by..." or "Partners" section
- **Need:** 4-8 logo images of customers or partners
- **Dimensions:** Variable, but uniform height (e.g., 80px high)
- **Style:** Grayscale or white versions for consistency
- **Format:** PNG with transparent background

### 6. Certification Badges
- **Examples:**
  - ESA compliance badge
  - ISO certifications
  - Industry standards badges
- **Dimensions:** Variable (typically 100-150px)
- **Format:** PNG with transparent background

## 💡 Nice to Have (Future Enhancements)

### 7. Video Demo
- **Purpose:** Replace one image placeholder with embedded video
- **Length:** 1-3 minutes
- **Content:** Platform walkthrough or mission simulation demo
- **Hosting:** YouTube, Vimeo, or self-hosted

### 8. Single Background Image (NEW! - Recommended)
- **File:** `background.jpg`
- **Purpose:** Single fixed background image for the entire website with parallax effect
- **Dimensions:** 1920x1080px or higher (2560x1440px recommended for larger screens)
- **Content suggestions:**
  - Satellite in orbit with Earth in background
  - Mission control center
  - Space/deep space view
  - Abstract technical/space imagery
  - Blurred technical diagrams for depth
- **Style:**
  - Dark images work best
  - High contrast with interesting focal points
  - Should look good when darkened (85% overlay applied)
  - Avoid busy patterns that might distract from text
- **Format:** JPG or WebP, optimized for web (< 800KB)
- **Location in code:** Line 560 in index.html
- **How to use:**
  1. Save your image as `background.jpg` in the website directory
  2. The site will automatically display it with:
     - Parallax scrolling effect
     - Dark overlay for text readability
     - Purple/coral gradient highlights
     - Floating particles on top

**Current setup:** Without a custom image, the site displays:
- Subtle animated gradient background (purple/coral)
- 30 floating particle effects
- Clean professional appearance

**Tip:** Try a dramatic space image - the heavy darkening ensures it won't interfere with readability!

### 9. Case Study Documents
- **Purpose:** Downloadable PDFs or dedicated landing pages
- **Examples:**
  - "How [Company] reduced validation time by 40%"
  - Technical whitepaper
  - Implementation guide
- **Format:** PDF

### 10. Additional Product Screenshots
- **Purpose:** Gallery or carousel showing different features
- **Content:**
  - Dashboard views
  - Test coverage reports
  - Integration interfaces
  - Analytics visualizations
- **Dimensions:** 16:9 aspect ratio
- **Format:** PNG or WebP

### 11. Mission Badge Graphics
- **Purpose:** Visual representation of HSD, HELEO, ERMIS missions
- **Dimensions:** Square or circular (200-300px)
- **Style:** Consistent with brand gradient colors
- **Format:** PNG with transparent background

## 📐 Technical Specifications

### Image Optimization Guidelines
- **Max file size:**
  - Hero images: < 500KB
  - Screenshots: < 300KB
  - Logos: < 50KB
  - Icons: < 20KB
- **Compression:** Use TinyPNG, ImageOptim, or similar
- **Format recommendations:**
  - Photos: JPG or WebP
  - Graphics/logos: PNG or SVG
  - Icons: SVG preferred

### Color Palette Reference
Your brand colors are already integrated:
- Purple: `#b7a9c9`
- Coral: `#e25c3f`
- Black: `#000000`
- White: `#ffffff`

Use these colors in any graphics you create for consistency.

## 🔧 How to Add Assets

### For Images:
1. Place image files in `/home/ggalanos/website/` directory
2. Update the corresponding `<img>` tag or placeholder in `index.html`
3. Example:
   ```html
   <!-- Replace this placeholder div -->
   <div style="aspect-ratio: 16/9; background: var(--odes-dark);">

   <!-- With this -->
   <img src="operational-simulator.png" alt="ODES Operational Simulator" style="width: 100%; border-radius: 4px;">
   ```

### For Testimonials:
1. Replace the placeholder text in lines 775-789
2. Keep the HTML structure intact
3. Update quote, name, and role for each testimonial

### For Team Photos:
1. Add image files: `giorgos.jpg`, `orestis.jpg`, `romanos.jpg`, `nikos.jpg`
2. Add `<img>` tags before each team member's `<h4>` tag
3. Example:
   ```html
   <div class="team-card">
       <img src="giorgos.jpg" alt="Giorgos Galanos" style="width: 120px; height: 120px; border-radius: 50%; margin-bottom: 1rem; object-fit: cover;">
       <h4>Giorgos Galanos</h4>
       ...
   ```

## ✅ Immediate Action Items

**To launch with a polished website, prioritize:**
1. ✅ Favicon (already generated: `favicon.png`)
2. 📸 Social card image (`odes-social-card.png`)
3. 💬 Three customer testimonials
4. 🖼️ Two product/facility images (simulator + integration)

**Optional but recommended:**
5. 👤 Team photos
6. 🏢 Customer/partner logos

---

**Questions or need help?** Let me know which assets you have available, and I can help integrate them into the website.
