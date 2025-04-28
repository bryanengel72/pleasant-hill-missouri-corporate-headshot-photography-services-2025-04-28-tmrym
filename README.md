# 101Headshots Landing Page Maintenance Guide

This guide will help you maintain and customize the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="/" class="text-xl font-bold tracking-tight">101Headshots</a>
```
- Replace "101Headshots" with your desired text
- The `text-xl` class controls size
- `tracking-tight` affects letter spacing

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-gray-900">Services</a>
    <!-- Other menu items -->
</div>
```
- Update text between `<a>` tags
- `text-gray-600` controls normal text color
- `hover:text-gray-900` controls hover state color

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight">
    Pleasant Hill, Missouri Corporate Headshot Photography Services
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Creating brand stories for Pleasant Hill entrepreneurs.
</p>
```
- Update text while maintaining the heading structure
- Size classes (`text-4xl`, etc.) are responsive:
  - `text-4xl`: Mobile devices
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Service Cards
Each service card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8">
    <h3 class="text-xl font-semibold mb-4">Story Shots</h3>
    <p class="text-gray-600">Professional headshots that tell...</p>
</div>
```
To modify:
1. Update the title in `<h3>` tags
2. Change description text in `<p>` tags
3. Keep the existing classes for consistent styling

## Managing Links

### Navigation Links
Current internal links in the navigation:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. The `#` symbol indicates section IDs on the same page
2. Match these with corresponding `id` attributes in sections
3. For external links, replace with full URLs:
```html
<a href="https://www.yoursite.com/services">Services</a>
```

### Call-to-Action Buttons
Current booking button:
```html
<a href="https://www.101headshots.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Book Your Session
</a>
```
To update:
1. Replace the URL in `href`
2. Maintain the classes for consistent styling
3. Update button text as needed

## Adding Privacy and Terms Pages

### Footer Links
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
</ul>
```

To add proper links:
1. Create privacy.html and terms.html files
2. Update the links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

For absolute URLs:
```html
<li><a href="https://www.101headshots.com/privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Verify section IDs match navigation links
- Check for typos in href attributes
- Ensure sections have corresponding ID attributes

2. **Responsive Design Issues**
- Don't remove responsive classes (md:, lg:)
- Keep the mobile-first approach
- Test on different screen sizes

3. **Style Inconsistencies**
- Maintain Tailwind CSS class structure
- Copy existing patterns for new elements
- Use browser inspector to verify styles

### Need Help?
If you encounter issues:
1. Check the Tailwind CSS documentation
2. Verify HTML syntax
3. Test in multiple browsers
4. Use browser developer tools to inspect elements

Remember to always backup your files before making changes, and test updates in a development environment first.