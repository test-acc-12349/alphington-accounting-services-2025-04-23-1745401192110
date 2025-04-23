# Alphington Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Alphington Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page is divided into these key sections:
- Header/Navigation (fixed at top)
- Hero Section (blue gradient background)
- Services Section
- Benefits Section
- FAQ Section
- Call-to-Action Section
- Footer

### Updating Text Content

#### Hero Section
```html
<!-- Located in the first section after <main> -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    We transform numbers into opportunities
</h1>
```
To modify the main headline, simply replace the text between the `<h1>` tags.

#### Services Cards
Each service card follows this structure:
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Dedicated Manager</h3>
    <p class="text-gray-600">Your personal financial advisor...</p>
</div>
```
To update service descriptions:
1. Locate the service cards in the `services` section
2. Modify the text within the `<h3>` and `<p>` tags
3. Maintain the existing classes to preserve styling

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
The page uses Tailwind's responsive prefixes:
- `md:` applies styles on medium screens (768px and up)
- `lg:` applies styles on large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Default size: text-4xl (36px)
- Medium screens: text-5xl (48px)
- Large screens: text-6xl (60px)

#### Common Tailwind Classes Used
- Spacing: `px-6`, `py-4`, `mb-6` (padding and margin)
- Colors: `text-blue-600`, `bg-white`, `text-gray-900`
- Flex: `flex`, `items-center`, `justify-between`
- Transitions: `transition-colors`, `duration-300`

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update internal links:
1. Locate the `href` attribute
2. Ensure it matches the `id` of the target section
3. For external links, replace with full URL

### Call-to-Action Links
Current placeholder:
```html
<a href="https://theaccountants.com" class="inline-block px-8 py-4 bg-blue-600">
```

To update:
1. Replace `https://theaccountants.com` with your actual URL
2. Test the link after updating
3. Maintain all existing classes

## Linking Privacy and Terms Pages

### Footer Links Section
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - Example: `href="#services"` must match `id="services"`

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Ensure `md:` and `lg:` classes are properly set
   - Test all breakpoints

3. **Missing Styles**
   - Verify Tailwind CDN is loading
   - Check for typos in class names
   - Ensure all closing tags are present

### Getting Help
- Consult [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser dev tools to inspect elements
- Test all changes in multiple browsers

Remember to always backup your code before making significant changes, and test thoroughly across different devices and screen sizes.