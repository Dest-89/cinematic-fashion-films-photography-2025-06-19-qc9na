# Landing Page Maintenance Guide

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold tracking-tighter text-white">SENTOE</a>
```
- Replace "SENTOE" with your brand name
- Adjust text size using `text-2xl` (can be `text-xl` for smaller or `text-3xl` for larger)

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Services</a>
```
- Replace "Services" with your desired menu text
- Keep the `text-gray-300` and `hover:text-white` classes for consistent styling

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8 bg-clip-text text-transparent bg-gradient-to-r from-purple-400 to-pink-400">
    Cinematic Fashion Films & Photography
</h1>
```
- Update the headline text between the `<h1>` tags
- The classes control:
  - `text-4xl`: Base text size
  - `md:text-6xl`: Tablet size
  - `lg:text-7xl`: Desktop size
  - `bg-gradient-to-r`: Creates the gradient effect

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-900 rounded-2xl p-8 hover:scale-105 transition duration-300 ease-in-out shadow-xl">
    <h3 class="text-xl font-semibold mb-4">NYC Based & Focused</h3>
    <p class="text-gray-400">Capturing the essence of New York City...</p>
</div>
```
- Update the `<h3>` text for feature titles
- Modify the description text in the `<p>` tag
- Keep the `hover:scale-105` class for the hover animation

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. The `#` symbol indicates an internal section link
2. Ensure the href matches the `id` of the target section
3. For external links, replace with full URL:
```html
<a href="https://yoursite.com/services">Services</a>
```

### Call-to-Action Buttons
Current booking button:
```html
<a href="https://sentoefilms.com" class="inline-block bg-gradient-to-r from-purple-500 to-pink-500...">
```
To update:
1. Replace `https://sentoefilms.com` with your booking page URL
2. Test the link after updating

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition duration-300">Terms of Service</a></li>
</ul>
```

To add proper links:
1. Create your privacy.html and terms.html pages
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-duration-300">Terms of Service</a></li>
```

For absolute URLs:
```html
<li><a href="https://yoursite.com/privacy.html">Privacy Policy</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Internal Links:**
   - Ensure section `id` attributes match the href values
   - Check for typos in the href attributes
   - IDs are case-sensitive

2. **Responsive Design Issues:**
   - If text appears too large/small, adjust the responsive classes:
     ```html
     <!-- Original -->
     <h1 class="text-4xl md:text-6xl lg:text-7xl">
     
     <!-- Smaller sizes -->
     <h1 class="text-3xl md:text-5xl lg:text-6xl">
     ```

3. **Gradient Text Not Showing:**
   - Ensure all these classes are present:
     ```html
     text-transparent bg-clip-text bg-gradient-to-r from-purple-400 to-pink-400
     ```

### Need Help?
- Double-check all closing tags
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test on multiple devices and browsers
- Keep backup copies before making changes

Remember to test all changes in a development environment before pushing to production.