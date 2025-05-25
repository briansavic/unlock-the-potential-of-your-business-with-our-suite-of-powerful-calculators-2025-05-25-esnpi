# Business Calculator Suite Landing Page - Maintenance Guide

This guide will help you maintain and customize the Business Calculator Suite landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To modify:

1. Update the brand name:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">Calculator<span class="text-gray-800">Suite</span></a>
```
- Change "Calculator" and "Suite" to your desired brand name
- Keep the `<span>` tag to maintain the two-tone color effect

2. Navigation menu items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Add or modify menu items here -->
</div>
```

### Hero Section
The main headline and subtitle can be updated here:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Unlock the potential of your business with our suite of powerful calculators
</h1>
```
- Replace the text between the `<h1>` tags
- Keep the existing classes to maintain responsive sizing
- The `md:` and `lg:` prefixes control how text appears on different screen sizes

### Tailwind CSS Tips for Beginners
Common classes used in this template:
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-blue-600`, `bg-white`, `text-gray-900`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-4` (margin bottom)
- Flex layout: `flex`, `items-center`, `justify-between`

## Managing Links

### Navigation Menu Links
Current internal links that need verification:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Ensure section IDs match these href values
2. For external pages, replace "#" with full URLs
3. Example: `<a href="https://yoursite.com/features">Features</a>`

### Call-to-Action Buttons
Current placeholder links to update:
```html
<!-- Replace all instances of "briansavic.com" with your actual URL -->
<a href="briansavic.com" class="inline-block px-6 py-2 bg-blue-600 text-white rounded-full">
```

### Email Links
Update the email address in the footer:
```html
<a href="mailto:briansavic@me.com" class="text-blue-400 hover:text-blue-300">
    briansavic@me.com
</a>
```

## Adding Privacy and Terms Pages

### Footer Legal Links
Current placeholder structure:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html files in your project
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly (case-sensitive)
   - Example: `href="#Features"` won't link to `id="features"`

2. **Responsive Design Issues**
   - If text overlaps on mobile:
     - Add responsive classes: `text-base md:text-lg lg:text-xl`
   - If elements stack incorrectly:
     - Check grid classes: `grid-cols-1 md:grid-cols-2 lg:grid-cols-3`

3. **Animation Not Working**
   - Verify AOS script is loaded
   - Check data-aos attributes:
```html
<div data-aos="fade-up" data-aos-delay="100">
```

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12 key)
2. Verify all script sources are accessible
3. Ensure Tailwind CSS CDN is loading properly
4. Test on multiple browsers and devices

Remember to always backup your files before making significant changes to the code.