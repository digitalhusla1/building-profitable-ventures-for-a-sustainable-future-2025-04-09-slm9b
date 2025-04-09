# AES Ventures Landing Page - Maintenance Guide

This guide will help you maintain and customize the AES Ventures landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. Company Name:
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    AES Ventures  <!-- Change this text -->
</a>
```

2. Navigation Menu Items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Change menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Update the main headline and subtext:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    Building Profitable Ventures for a Sustainable Future  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    AES Ventures: Turning ideas into success.  <!-- Subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:
- `text-{size}`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-{size}`: Adds margin bottom (e.g., `mb-6`, `mb-12`)
- `py-{size}`: Adds padding top and bottom
- `px-{size}`: Adds padding left and right
- `bg-{color}`: Sets background color
- `hover:`: Adds hover effects (e.g., `hover:text-white`)

Example of modifying a button:
```html
<!-- Original button -->
<a href="https://www.aesventures.com" class="inline-block px-8 py-4 text-lg font-semibold rounded-full bg-gradient-to-r from-purple-600 to-pink-600">

<!-- To make button larger -->
<a href="https://www.aesventures.com" class="inline-block px-10 py-5 text-xl font-semibold rounded-full bg-gradient-to-r from-purple-600 to-pink-600">
```

## Managing Links

### Internal Navigation Links
Current internal links use anchor tags (#):
```html
<!-- In the navigation menu -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update these:
1. Find the section ID in the HTML:
```html
<section id="features" class="py-24 px-6 bg-gray-800/50">
```
2. Make sure the href matches the ID:
```html
<a href="#features">Features</a>
```

### External Links
The main external link is the "Get Started" button:
```html
<a href="https://www.aesventures.com" class="inline-block px-8 py-4...">
    Get Started
</a>
```

To update:
1. Replace `https://www.aesventures.com` with your desired URL
2. Test the link to ensure it works
3. Consider adding `target="_blank"` to open in a new tab:
```html
<a href="https://www.aesventures.com" target="_blank" class="inline-block px-8 py-4...">
```

## Adding Privacy and Terms Pages

### Footer Links
Current placeholder links in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-6">Legal</h4>
    <ul class="space-y-4">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To link to actual pages:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

For consistency, use the same styling classes on your new pages:
```html
<a href="index.html" class="text-gray-400 hover:text-white transition-colors duration-300">
    Back to Home
</a>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Styling Issues**
   - Make sure Tailwind CSS is properly loaded
   - Check for typos in class names
   - Use browser inspector to verify classes are applied

3. **Responsive Design**
   - Test on different screen sizes
   - Look for classes starting with `md:` or `lg:` for responsive behavior
   - Don't remove these responsive classes unless you're sure about the impact

Remember to:
- Always backup your code before making changes
- Test all links after updating
- View the page on different devices to ensure responsive design works
- Keep the original code as reference until your changes are verified