# Ultimate Cars Landing Page - Maintenance Guide

This guide will help you maintain and customize the Ultimate Cars landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. Company Name:
```html
<div class="text-2xl font-bold tracking-tight">
    Ultimate Cars  <!-- Change this text -->
</div>
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
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tighter mb-8">
    It Doesn't Have To Be New To Be Better!  <!-- Update main headline -->
</h1>
<p class="text-xl text-gray-600 mb-12">
    Experience premium pre-owned vehicles with confidence and peace of mind.  <!-- Update subheading -->
</p>
```

### Tailwind CSS Tips
- Font sizes use classes like `text-xl`, `text-2xl`, etc.
- Colors use format `text-gray-600` or `bg-gray-900`
- Spacing uses `m` (margin) or `p` (padding) with numbers (4 = 1rem)
- Responsive classes start with `md:` or `lg:`

Example: To make text larger on mobile:
```html
<!-- Original -->
<h3 class="text-xl font-semibold mb-4">

<!-- Modified for larger mobile text -->
<h3 class="text-2xl md:text-xl font-semibold mb-4">
```

## Managing Links

### Current Link Locations

1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Buttons:
```html
<!-- Replace google.com with your inventory page URL -->
<a href="https://google.com" class="inline-block bg-gray-900 text-white px-8 py-4 rounded-lg">
    Browse Our Inventory
</a>
```

### Updating Links

1. For internal page sections:
```html
<a href="#section-name">Link Text</a>
```

2. For external pages:
```html
<a href="https://your-full-url.com">Link Text</a>
```

3. For local pages:
```html
<a href="./about.html">Link Text</a>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Files
Create two new files in your project folder:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2 text-gray-600">
        <!-- Update these href attributes -->
        <li><a href="./privacy.html" class="hover:text-gray-900">Privacy Policy</a></li>
        <li><a href="./terms.html" class="hover:text-gray-900">Terms of Service</a></li>
    </ul>
</div>
```

### Step 3: Maintain Consistent Styling
Copy these classes for new links to match existing styling:
```html
class="hover:text-gray-900"
```

## Troubleshooting

### Common Issues

1. Broken Links
- Check for typos in `href` attributes
- Verify file names match exactly
- Ensure files are in the correct directory

2. Styling Problems
- Check for missing class names
- Verify Tailwind CDN is loading
- Inspect element using browser dev tools (F12)

3. Responsive Issues
- Test at different screen sizes
- Verify `md:` and `lg:` classes are correct
- Check for missing responsive classes

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Compare changes against the original code
- Test all changes in multiple browsers

Remember to:
- Back up files before making changes
- Test all links after updating
- View changes on multiple devices
- Keep consistent styling throughout
- Maintain proper indentation for readability