# Boston Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Boston Web Design landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo text. To update:

1. **Logo Text**: Find this line in the header:
```html
<a href="/" class="text-2xl font-bold text-gray-800">Boston Web Design</a>
```
Simply replace "Boston Web Design" with your desired text.

2. **Navigation Items**: Located in the `<div class="hidden md:flex space-x-8">` section:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
Update the text between `<a>` tags to change menu items.

### Hero Section
Find the main headline and subtext:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Best Websites In Boston
</h1>
<p class="text-xl text-gray-600">
    Professional web design services tailored for Boston businesses
</p>
```
- Change the text while keeping the surrounding tags intact
- The classes `text-4xl`, `md:text-5xl`, and `lg:text-6xl` control text size at different screen sizes

### Features and Benefits
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-server text-4xl"></i>
    </div>
    <h3 class="text-xl font-bold">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included...</p>
</div>
```
To modify:
1. Change the icon by updating the `fas fa-server` class to another [Font Awesome icon](https://fontawesome.com/icons)
2. Update the heading text in the `<h3>` tag
3. Modify the description in the `<p>` tag

## Managing Links

### Navigation Links
Current internal links use anchor tags (#):
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
```
To link to external pages:
1. Replace the `#` with full URLs
2. Example: `<a href="https://example.com/features">Features</a>`

### Call-to-Action Button
Located in the hero section:
```html
<a href="https://twd.com" class="inline-block bg-blue-600 text-white px-8 py-4">
    Get Started Today
</a>
```
Replace `https://twd.com` with your desired URL.

### Social Media Links
Found in the footer:
```html
<a href="#" class="text-gray-400 hover:text-white">
    <i class="fab fa-twitter text-xl"></i>
</a>
```
Replace the `#` with your social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Insert these lines in the footer's Quick Links section:
```html
<li>
    <a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">
        Privacy Policy
    </a>
</li>
<li>
    <a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">
        Terms of Service
    </a>
</li>
```

### Step 2: Create Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Layout**
- Check that all `<div>` tags are properly closed
- Verify Tailwind CSS classes are spelled correctly
- Ensure the Tailwind CDN link is working:
```html
<script src="https://cdn.tailwindcss.com"></script>
```

2. **Missing Icons**
- Confirm Font Awesome CDN is loaded:
```html
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
```
- Verify icon class names match Font Awesome documentation

3. **Responsive Issues**
- Check media query classes (md:, lg:)
- Test on different screen sizes
- Ensure the viewport meta tag is present:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Need Help?
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Check Tailwind documentation for class references
- Inspect elements using browser developer tools (F12)

Remember to always test changes across different devices and browsers before publishing updates.