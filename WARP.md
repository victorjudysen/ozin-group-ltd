# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

This is a modern, single-page website for **Ozin Group Limited**, a Class 3 building contractor based in Dodoma, Tanzania. The project showcases the company's services, credentials, and professional excellence through an interactive web experience.

**Key Business Details:**
- Company: Ozin Group Limited
- Registration: B3/162/03/2024 (Class 3 Licensed Contractor)
- Managing Director: Omary Chuguma
- Location: P.O. BOX 913, Dodoma, Tanzania
- Contact: +255 743 010 010, info@ozingroup.co.tz

## Technology Stack & Architecture

### Frontend Architecture
- **Technology**: Pure HTML5, CSS3, JavaScript (ES6+)
- **Dependencies**: 
  - Google Fonts (Inter typeface)
  - Font Awesome 6.4.0 (icons)
  - No frameworks or build tools required
- **Browser Support**: Modern browsers with ES6+ support

### File Structure
```
ozin-group-ltd/
├── index.html          # Main HTML file with complete site structure
├── styles.css          # Comprehensive stylesheet with advanced CSS animations
├── script.js           # Interactive JavaScript with modern features
├── .vscode/
│   └── settings.json   # VS Code configuration (Live Server on port 5501)
├── .git/               # Git repository
└── WARP.md            # This file
```

## High-Level Code Architecture

### 1. Welcome Loader System (`styles.css` lines 52-900)
An elaborate construction-themed loading animation featuring:
- **Animated Construction Scene**: Cranes, buildings, workers, equipment
- **Interactive Elements**: Floating construction tools, particle systems
- **Progress System**: Animated progress bar with construction truck
- **Dynamic Messaging**: Rotating highlight messages during load

### 2. Modern JavaScript Architecture (`script.js`)
Modular JavaScript with clear separation of concerns:
- **Initialization**: `initializeApp()` orchestrates all components
- **Animation Systems**: Parallax, particle effects, reveal animations
- **Interactive Components**: Navigation, forms, scroll effects
- **Performance Optimization**: Throttled scroll events, intersection observers
- **Accessibility Features**: Skip links, keyboard navigation, reduced motion

### 3. CSS Design System
Professional design system with:
- **CSS Custom Properties**: Comprehensive color palette, typography scales
- **Component-Based Styles**: Reusable classes and consistent spacing
- **Advanced Animations**: Construction-themed keyframe animations
- **Responsive Design**: Mobile-first approach with breakpoint system

### 4. Single-Page Application Structure
Content sections managed through:
- **Smooth Scrolling Navigation**: JavaScript-powered with active state tracking
- **Section-Based Layout**: Home, About, Services, Projects, Credentials, Contact
- **Interactive Forms**: Contact form with validation and notification system

## Development Commands

### Local Development
```powershell
# Start local development server (if Live Server extension installed in VS Code)
# The project is configured to run on port 5501
# Simply open index.html with Live Server or any static file server

# Alternative: Using Python (if available)
python -m http.server 8000
# Then navigate to http://localhost:8000

# Alternative: Using Node.js serve package (if available)
npx serve .
```

### Git Workflow
```powershell
# Check current status
git status

# Stage changes
git add .

# Commit with descriptive message (following project pattern)
git commit -m "DD.MMM: Description of changes"

# Push to remote
git push origin main

# Pull latest changes
git pull origin main
```

### File Operations
```powershell
# View project structure
Get-ChildItem -Recurse -Name

# Search for specific content
Select-String -Path "*.html","*.css","*.js" -Pattern "search-term"

# Check file sizes (useful for performance)
Get-ChildItem -File | Select-Object Name, @{Name='Size(KB)';Expression={[math]::Round($_.Length/1KB,2)}}
```

## Code Architecture Notes

### JavaScript Module Pattern
The codebase uses a functional approach with clear initialization sequence:
1. **DOM Ready**: Event listener triggers `initializeApp()`
2. **Component Initialization**: Each feature has its own `init*()` function
3. **Event Binding**: Throttled scroll events and optimized listeners
4. **Animation Systems**: Intersection observers for performance

### CSS Architecture Highlights
- **Construction Theme**: Elaborate loading animations mimicking construction site
- **CSS Grid & Flexbox**: Modern layout techniques throughout
- **Custom Properties**: Consistent design tokens for colors, spacing, typography
- **Performance**: Hardware-accelerated animations using transforms

### Key JavaScript Features
- **Welcome Loader**: Complex construction scene with multiple animated elements
- **Smooth Scrolling**: Custom easing functions for navigation
- **Parallax Effects**: Mouse and scroll-based parallax for interactive elements
- **Form Handling**: Complete form validation with notification system
- **Accessibility**: Skip links, keyboard navigation, reduced motion support

### Notable Technical Implementations
- **Particle System**: Canvas-based particle effects in hero section
- **Dynamic Animations**: Staggered reveal animations with intersection observers
- **Performance Optimization**: Throttled scroll events and lazy loading patterns
- **Mobile Responsiveness**: Touch-friendly navigation with animated mobile menu

## Content Management

### Business Information Updates
When updating company information, modify these key areas:
- **HTML Meta Tags**: Update title, description, keywords in `<head>`
- **Contact Information**: Multiple instances throughout HTML (header, contact section, footer)
- **Professional Credentials**: Registration numbers and certifications in credentials section
- **Service Offerings**: Services grid section with detailed descriptions

### Visual Content
- **Icons**: Font Awesome classes used throughout for construction-themed icons
- **Colors**: Defined in CSS custom properties, easy to rebrand
- **Typography**: Inter font family used consistently across the site

## Deployment

This is a static website that can be deployed to any web server:

### Hosting Options
- **GitHub Pages**: Already connected to `https://github.com/victorjudysen/ozin-group-ltd.git`
- **Netlify**: Drag and drop deployment
- **Vercel**: Connect GitHub repository
- **Traditional Web Hosting**: Upload files via FTP

### Pre-Deployment Checklist
1. **Test all animations**: Ensure welcome loader completes properly
2. **Validate forms**: Test contact form submission and validation
3. **Check responsiveness**: Test on mobile devices and different screen sizes
4. **Verify links**: Ensure all navigation links work correctly
5. **Performance check**: Optimize images if any are added

## Project Context

This website represents a professional construction company's digital presence with emphasis on:
- **Professional Credibility**: Detailed credentials and registration information
- **Service Excellence**: Comprehensive service descriptions and project showcases  
- **Modern Technology**: Advanced web animations and interactive features
- **Local Market**: Specifically tailored for Tanzanian construction market

The codebase demonstrates advanced front-end development techniques while maintaining simplicity and performance for a business website in the construction industry.
