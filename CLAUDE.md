# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the marketing website for "Doctor Assistance" (DRAssistance), a medical assistant application for healthcare professionals. The website is built as a static HTML site targeting Chinese (Traditional) speaking medical professionals.

## Architecture & Structure

### Technology Stack
- **Frontend**: Pure HTML5, CSS3 with modern CSS Grid/Flexbox, and vanilla JavaScript
- **Styling**: Custom CSS variables for theming, responsive design with mobile-first approach
- **Language**: Traditional Chinese (zh-TW) as primary language
- **Assets**: Local images in `screenshots/` directory for app demonstrations

### Core Pages
- `index.html` - Main landing page with feature showcase and product demonstration
- `security.html` - Detailed security features and encryption specifications
- `support.html` - Technical support, FAQ, and contact information
- `privacy-policy.html` - Privacy policy (referenced but not present)
- `terms.html` - Terms of service (referenced but not present)

### Key Components

#### Design System
- **Color Palette**: Blue/cyan primary colors with emerald accents for medical branding
- **Typography**: Inter font family for modern, professional appearance
- **Icons**: Emoji-based icons for simplicity and international compatibility
- **Layout**: CSS Grid for complex layouts, Flexbox for component alignment

#### Responsive Design
- **Breakpoints**: 768px (mobile), 1024px (tablet), with specific handling for 480px (small mobile)
- **Navigation**: Collapsible mobile menu with hamburger button
- **Grid Systems**: Auto-fit minmax patterns for flexible responsive grids

#### Interactive Features
- Smooth scrolling navigation with scroll-triggered animations
- Dynamic navbar with scroll effects and backdrop blur
- Mobile menu toggle with outside-click dismissal
- Animated elements using CSS keyframes and JavaScript intersection observers

### Content Architecture

#### Medical App Features
The website showcases a medical assistant app with these core features:
- **Patient Management**: List view with bed numbers and priority marking
- **Task Management**: Manual task creation with priority levels and categories
- **Apple Pencil Support**: iPad-specific handwriting input for quick note-taking during rounds
- **Security**: AES-256-GCM encryption for sensitive patient data

#### Security Focus
- Detailed technical specifications for medical-grade encryption
- Clear data classification (encrypted vs. plaintext)
- Compliance with medical privacy standards
- Technical architecture documentation

## Development Guidelines

### File Management
- All HTML files should maintain consistent navigation structure
- Image assets go in `screenshots/` directory
- Icon file is `icon.png` at root level
- All text content should be in Traditional Chinese

### CSS Architecture
- Use CSS custom properties (variables) defined in `:root`
- Follow existing naming conventions (BEM-like approach)
- Maintain responsive design patterns
- Keep consistent spacing and color schemes

### Content Updates
- Medical content requires accuracy and professional tone
- Security specifications should be technically precise
- All features mentioned should align with the actual app capabilities
- Contact information: mses98034@gmail.com

### Browser Support
- Modern browsers with CSS Grid and Flexbox support
- JavaScript ES6+ features used
- Progressive Web App (PWA) capabilities mentioned
- iPad-specific Apple Pencil support for handwriting features

## Common Tasks

### Adding New Pages
1. Copy navigation structure from existing pages
2. Maintain consistent header/footer
3. Use established CSS classes and design patterns
4. Ensure responsive design at all breakpoints

### Updating Content
- Maintain professional medical terminology
- Keep Traditional Chinese language consistency
- Update copyright year when needed (currently 2025)
- Ensure all internal links remain functional

### Asset Management
- Compress images for web delivery
- Maintain consistent screenshot aspect ratios
- Use `alt` attributes for accessibility
- Keep file sizes optimized for mobile users

## Technical Notes

### Performance
- No external dependencies beyond Google Fonts
- Inline CSS to reduce HTTP requests
- Optimized images and minimal JavaScript
- Smooth animations with hardware acceleration

### SEO & Accessibility
- Semantic HTML structure
- Proper meta tags and descriptions
- Alt text for images
- Focus management for mobile menu
- Proper heading hierarchy

### Security Considerations
- No external tracking scripts
- HTTPS references only
- No inline event handlers
- CSP-friendly code structure