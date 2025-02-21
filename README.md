# SergerPro Landing Page Maintenance Guide

This guide will help you maintain and customize the SergerPro landing page. Whether you're new to HTML and CSS or just getting started with web development, follow these instructions to make updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**: Find this line and change "SergerPro" to your desired text:
```html
<a href="#" class="text-2xl font-bold text-indigo-600">SergerPro</a>
```

2. **Navigation Menu Items**: Located in the header `<nav>` section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">FAQ</a>
</div>
```

### Hero Section
The main headline and subtitle are in the first `<section>` after `<main>`:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    Unlock the Secrets of Your Serger – Sew Like a Pro with Confidence
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    ✨ Unlock Your Serger's Full Potential – Sew Like a Pro! ✨
</p>
```

### Tailwind CSS Class Guide
Common classes used throughout the page:

- Text sizes: `text-xl`, `text-2xl`, `text-3xl`, etc.
- Colors: `text-indigo-600`, `bg-white`, `text-gray-600`
- Spacing: `mb-6` (margin-bottom), `px-6` (padding-x), `py-4` (padding-y)
- Responsive design: `md:text-2xl` (applies at medium screens and up)

To modify styles:
1. Find the element you want to change
2. Locate its `class=""` attribute
3. Add or modify Tailwind classes within the quotes
4. Multiple classes are separated by spaces

Example:
```html
<!-- Original -->
<p class="text-xl text-gray-600">

<!-- Modified for larger, blue text -->
<p class="text-2xl text-blue-600">
```

## Managing Links

### Navigation Links
The page uses anchor links to scroll to sections:

```html
<!-- In the navigation menu -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>

<!-- Corresponding section IDs -->
<section id="features">
<section id="benefits">
<section id="faq">
```

### Call-to-Action Links
The main CTA buttons currently point to a Digistore24 link. Update these by finding:

```html
<a href="https://www.digistore24.com/redir/561361/BetoWH72/">
```

Replace with your new link:
```html
<a href="https://your-new-link.com">
```

### Social Media Links
Located in the footer section:

```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white transition-colors duration-300">
        <!-- Facebook icon -->
    </a>
    <a href="#" class="hover:text-white transition-colors duration-300">
        <!-- Instagram icon -->
    </a>
</div>
```

Replace the `#` with your social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Create New Files
1. Create two new files in your project folder:
   - `privacy.html`
   - `terms.html`

### Step 2: Update Footer Links
Find this section in the footer:

```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - Check for typos in both the link and section ID
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Look for classes starting with `md:` or `lg:`
   - These control how elements appear on different screen sizes
   - Test your page at various browser widths

3. **Styling Problems**
   - Check for missing spaces between Tailwind classes
   - Verify class names match Tailwind's naming convention
   - Use browser inspector to identify which styles are applied

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools (F12) to inspect elements
- Test all links before deploying changes
- Keep a backup of the original code before making changes

Remember to always test your changes across different devices and browsers to ensure everything works as expected.