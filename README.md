# VETOR Website

A modern, responsive single-page website for VETOR agricultural supplement products.

## Repository Structure

```
.
├── index.html                 # Main website file
├── css/                        # Local CSS files
│   ├── w3.css                # W3.CSS framework (v5.01)
│   └── font-awesome.min.css   # Font Awesome icons (v4.7.0)
├── fonts/                     # Font files (see notes below)
├── img/                       # All local images
│   ├── main.jpg              # Hero section background
│   ├── bg2.png               # Section background
│   ├── logo.png              # Header logo
│   ├── wachat-green.png      # WhatsApp contact button
│   ├── whatsapp-icon.svg     # WhatsApp floating button icon
│   ├── Defense.jpg           # Product image
│   ├── Root.jpg              # Product image
│   ├── Bloom.jpg             # Product image
│   ├── Fruit.jpg             # Product image
│   ├── durian.png            # Service showcase
│   ├── mango.png             # Service showcase
│   ├── cili.png              # Service showcase
│   ├── eggplant.png          # Service showcase
│   ├── peria.png             # Service showcase
│   ├── timun.png             # Service showcase
│   ├── strawberry.png        # Service showcase
│   └── melon.png             # Service showcase
├── Startup.txt               # Project notes
└── README.md                 # This file

## Local Resources

The following resources have been downloaded and stored locally to ensure the site is **repository-friendly** and works offline:

✅ **W3.CSS Framework** - Fully local
- File: `css/w3.css`
- Source: W3.CSS v5.01 (March 2026)
- Status: Ready to use

✅ **Font Awesome Icons** - Partially local
- File: `css/font-awesome.min.css`
- Note: Font files need to be downloaded separately (see below)
- Source: Font Awesome v4.7.0

✅ **WhatsApp Icons** - Fully local
- Files: `img/whatsapp-icon.svg`, `img/wachat-green.png`
- Status: Ready to use

✅ **All Images** - Fully local
- All product and service images are stored in `img/` directory
- Status: Ready to use

## External Dependencies (Still Required)

The following services are **external** and cannot be made fully local without licensing/hosting your own:

### 1. **Google Fonts - Raleway**
- **Type:** Web Font
- **Used for:** Primary font family
- **Fallback:** The site uses system fonts (Segoe UI, Arial, sans-serif) as fallback
- **To make fully local:** 
  1. Download the Raleway font family from https://fonts.google.com/specimen/Raleway
  2. Place font files in `fonts/` directory
  3. Create a `fonts/raleway.css` file with @font-face rules
  4. Update the import in `index.html` style section

### 2. **Google Maps Embed**
- **Type:** Embedded map/API
- **Location:** Contact section
- **URL:** `https://www.google.com/maps/d/embed?mid=...`
- **To replace:** 
  - Use alternative mapping services like Leaflet + OpenStreetMap
  - Or provide an address with alternative map link

### 3. **Formspree Contact Form**
- **Type:** Form processing service
- **URL:** `https://formspree.io/f/mjgpzykn`
- **To replace:**
  - Implement server-side form handling
  - Use alternative services like Netlify Forms or AWS Lambda
  - Or create a static contact form with backend integration

### 4. **Font Awesome Font Files**
- **Type:** Icon font files (must be hosted)
- **Files needed:** eot, woff2, woff, ttf, svg variants
- **To add:**
  1. Download from https://fontawesome.com/download
  2. Extract font files to `fonts/` directory
  3. Update CSS file path: `url('../fonts/fontawesome-webfont.xxx')`

## How to Use Font Awesome Locally

The Font Awesome CSS file is already set up to look for fonts in the `fonts/` directory. To make the icons work:

1. Download Font Awesome 4.7.0 from: https://fontawesome.com/download
2. Extract the font files (`.eot`, `.woff2`, `.woff`, `.ttf`, `.svg`)
3. Copy them to the `fonts/` directory
4. The icons should then display correctly

## Making the Site 100% Local

To make the site completely local with no external dependencies:

1. **Fonts:** 
   - Download Raleway from Google Fonts
   - Create a `fonts/raleway.css` file with @font-face declaration
   - Update HTML to use local font CSS

2. **Maps:**
   - Reference an offline mapping solution or static image
   - Or provide address in text format

3. **Forms:**
   - Implement server-side form handling
   - Or use JavaScript to store form submissions locally

4. **Font Awesome:**
   - Follow steps in "How to Use Font Awesome Locally" section above

## Browser Compatibility

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile responsive (tested on various viewport sizes)
- Graceful degradation for older browsers

## Notes

- All image paths use relative URLs (`/img/filename`)
- CSS files use relative paths for easy local deployment
- No build process required - pure HTML/CSS/JavaScript
- Icons fallback to system fonts if Font Awesome fonts are not available
- Raleway font gracefully falls back to system fonts if unavailable

## Updates Made for Local Compatibility

- ✅ Replaced CDN CSS links with local files
- ✅ Replaced external WhatsApp icon with local SVG
- ✅ Maintained all external API integrations (Maps, Forms) for functionality
- ✅ Added font fallbacks for better offline experience
- ✅ All images already stored locally

## Deployment

To deploy this site:

1. **As static site:** Copy all files to your web server
2. **Locally:** Simply open `index.html` in a browser (most features will work)
3. **With forms:** Use Formspree or set up server-side form handling
4. **With maps:** Replace Google Maps embed with alternative service

Enjoy! 🎉
