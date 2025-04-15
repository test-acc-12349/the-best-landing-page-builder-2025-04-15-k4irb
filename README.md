# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page. Whether you're new to web development or need a quick reference, follow these instructions to make updates while preserving the design integrity.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name**: Locate this line and change "PageBuilder":
```html
<a href="/" class="text-2xl font-bold text-blue-600">PageBuilder</a>
```

2. **Navigation Items**: Find these lines to modify menu items:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="https://sigmaseo.io">Get Started</a>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    The Best Landing Page Builder
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Create stunning landing pages in minutes
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-[size]`: Controls text size (xl, 2xl, etc.)
- `font-bold`: Makes text bold
- `mb-[size]`: Adds bottom margin (4, 6, 8, etc.)
- `py-[size]`: Adds vertical padding
- `px-[size]`: Adds horizontal padding
- `bg-[color]`: Sets background color

To modify styling:
1. Find the element you want to change
2. Locate its class attribute
3. Add or replace Tailwind classes

Example:
```html
<!-- Original -->
<div class="bg-white p-8 rounded-2xl">

<!-- Modified with different background and padding -->
<div class="bg-gray-50 p-12 rounded-2xl">
```

## Managing Links

### Navigation Links
Current navigation links are:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="https://sigmaseo.io">Get Started</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace with your new URL
3. For internal links, use `#section-id`
4. For external links, use complete URLs

Example:
```html
<!-- Change external link -->
<a href="https://your-website.com">Get Started</a>

<!-- Change internal link -->
<a href="#pricing">Pricing</a>
```

### Footer Links
Current footer links are placeholders. Update them in the footer section:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <!-- Each column contains links -->
    <ul class="space-y-2">
        <li><a href="#">About Us</a></li>
        <!-- Add more links here -->
    </ul>
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate these lines in the footer:
```html
<li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

Replace with:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in URLs
   - Ensure file names match exactly
   - Verify file locations in your project

2. **Styling Problems**
   - Check for missing classes
   - Verify Tailwind CSS is properly loaded
   - Ensure responsive classes (md:, lg:) are correct

3. **Mobile Menu Issues**
   - Verify Alpine.js is properly loaded
   - Check x-data and x-show attributes
   - Test on different screen sizes

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check [Alpine.js documentation](https://alpinejs.dev/docs) for menu functionality
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to test all changes across different devices and browsers before deploying to production.