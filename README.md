# Landing Page Maintenance Guide

This guide will help you maintain and customize the Hoogwerker Huren Drachten landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the main navigation and logo. To update:

1. **Company Name/Logo**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">Hoogwerker Drachten</a>
```
- Replace "Hoogwerker Drachten" with your company name
- Adjust text size using `text-2xl` (options: `text-xl`, `text-3xl`, etc.)
- Change color using `text-blue-600` (options: `text-red-600`, `text-green-600`, etc.)

2. **Navigation Menu Items**
```html
<a href="#features" class="text-gray-600 hover:text-blue-600">Diensten</a>
```
- Replace "Diensten" with your menu item name
- Keep the hover effect (`hover:text-blue-600`) for consistency

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Hoogwerker Huren Drachten
</h1>
```
- Update the text between the `<h1>` tags
- Responsive text sizes:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Promotional Banner
```html
<div class="mt-8 p-4 bg-yellow-100 rounded-lg inline-block">
    <p class="text-yellow-800 font-medium">
        🔥 Nog maar 3 hoogwerkers beschikbaar voor dit weekend!
    </p>
</div>
```
- Update the promotional text
- Change background color: replace `bg-yellow-100` with other colors
- Modify text color: replace `text-yellow-800` accordingly

## Fixing Broken Links

### Navigation Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Diensten</a>
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Internal links (same page sections):
   - Keep the `#` prefix
   - Ensure the ID matches your section: `href="#section-id"`

2. External links:
   - Replace `#` with full URL: `href="https://example.com"`
   - Example:
   ```html
   <a href="https://your-website.com/services" class="text-gray-600 hover:text-blue-600">
   ```

### Call-to-Action Buttons
```html
<a href="https://hansschuiling.nl" class="inline-flex items-center justify-center px-8 py-4 text-lg">
    Direct Huren
</a>
```
- Replace `https://hansschuiling.nl` with your booking URL
- Keep the styling classes to maintain design consistency

## Linking Privacy and Terms Pages

### Adding Footer Links
Locate the footer section and add privacy/terms links:

```html
<div class="mt-12 pt-8 border-t border-gray-800 text-center">
    <p class="text-gray-400">&copy; 2024 Hoogwerker Huren Drachten. Alle rechten voorbehouden.</p>
    <!-- Add these lines below the copyright notice -->
    <div class="mt-4 space-x-4">
        <a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">
            Privacy Policy
        </a>
        <a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">
            Terms & Conditions
        </a>
    </div>
</div>
```

### Creating New Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`
2. Use the same header and footer as `index.html`
3. Link back to home:
```html
<a href="/" class="text-blue-600 hover:text-blue-700">Back to Home</a>
```

## Troubleshooting

### Common Issues

1. **Broken Layout**
- Check for missing closing tags
- Verify Tailwind CSS classes are spelled correctly
- Ensure responsive classes (`md:`, `lg:`) are properly ordered

2. **Links Not Working**
- Verify href attributes start with `/`, `#`, or `https://`
- Check for typos in section IDs
- Ensure external URLs include `https://`

3. **Styling Issues**
- Confirm Tailwind CSS CDN link is working
- Check class names match Tailwind v2.2.19 syntax
- Test responsive breakpoints using browser dev tools

### Need Help?
- Review the [Tailwind CSS documentation](https://v2.tailwindcss.com/docs)
- Check browser console for errors
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to test all changes across different devices and browsers before deploying to production.