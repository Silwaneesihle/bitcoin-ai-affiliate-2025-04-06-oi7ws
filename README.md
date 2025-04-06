# Bitcoin AI Affiliate Landing Page - Maintenance Guide

This guide will help you maintain and customize the Bitcoin AI Affiliate landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update the logo text:

```html
<!-- Find this section near the top -->
<div class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Bitcoin AI Affiliate  <!-- Change this text -->
</div>
```

#### Navigation Menu Items
To modify navigation links, locate this section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Change text here -->
    <a href="#benefits">Benefits</a>  <!-- And here -->
    <!-- etc. -->
</div>
```

### Hero Section
The main headline and subtitle can be found here:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Discover how to earn Bitcoin using Artificial Intelligence  <!-- Main headline -->
</h1>
<p class="text-xl text-gray-600 mb-12">
    Leverage AI technology to generate passive Bitcoin income  <!-- Subtitle -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this page:
- `text-4xl`: Large text size
- `md:text-5xl`: Larger text on medium screens
- `mb-8`: Margin bottom spacing
- `bg-white`: White background
- `text-gray-600`: Gray colored text

To modify sizes or colors, replace the number values:
- Colors: `text-blue-600` → `text-blue-700` (darker) or `text-blue-500` (lighter)
- Spacing: `mb-8` → `mb-4` (smaller) or `mb-12` (larger)

## Fixing Broken Links

### Navigation Menu Links
Current internal links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update these:
1. Find the corresponding section ID in the HTML
2. Make sure the href matches exactly (including #)
3. Example: `<section id="features">` matches with `href="#features"`

### Call-to-Action Buttons
There are two main CTA buttons:
```html
<!-- Hero section button -->
<a href="https://go.e1ulife.com/ai-takeover?affid=Silwane1">Start Earning Bitcoin Now</a>

<!-- Bottom section button -->
<a href="https://go.e1ulife.com/ai-takeover?affid=Silwane1">Get Started Now</a>
```

To update these:
1. Replace the URL in `href=""`
2. Keep the button text relevant to your offer
3. Maintain the existing classes for consistent styling

## Linking Privacy and Terms Pages

### Footer Legal Links
Locate this section in the footer:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
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

### Common Issues:

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Must include # for internal links

2. **Responsive Design Issues**
   - Look for classes starting with `md:` or `lg:`
   - These control appearance on different screen sizes
   - Don't remove these classes unless you're sure

3. **Missing Styles**
   - Verify the Tailwind CDN link is present in the head section
   - Check for typos in class names
   - Tailwind classes must be exact matches

4. **Animation Problems**
   - Check that AOS script is loaded at bottom of page
   - Verify data-aos attributes are spelled correctly
   - Ensure AOS.init() is called in the script section

Remember to always test your changes across different screen sizes using browser developer tools (F12 in most browsers).

For additional help or specific questions, contact support or consult the Tailwind CSS documentation.