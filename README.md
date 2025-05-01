# Landing Page Maintenance Guide

This guide will help you maintain and customize the WebAgency landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

```html
<!-- Find this section at the top of the page -->
<a href="/" class="text-2xl font-bold text-white hover:text-blue-400">
    WebAgency  <!-- Replace this text with your company name -->
</a>
```

### Hero Section
Located at the top of the page, this section contains your main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Best Web Agency In Sydney  <!-- Replace with your headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Grow your business with clicks  <!-- Replace with your subheading -->
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout the page:
- `text-{size}`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `md:text-{size}`: Applies text size at medium screens and up
- `mb-{number}`: Adds margin bottom (e.g., `mb-8` = 2rem spacing)
- `py-{number}`: Adds padding top and bottom
- `px-{number}`: Adds padding left and right

To modify spacing, replace numbers:
```html
<!-- Example: Change padding from 6 to 8 -->
<div class="px-6 py-4">  <!-- Original -->
<div class="px-8 py-4">  <!-- Modified -->
```

## Managing Links

### Navigation Menu Links
The navigation menu contains internal links to page sections:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. For internal links, use `#section-name`
3. For external links, use full URL: `https://example.com`

### Call-to-Action Buttons
Currently points to "fixrr.online". Update these links:

```html
<!-- Find these buttons throughout the page -->
<a href="https://fixrr.online" class="inline-flex items-center...">
    Start Growing Today
</a>
```

Replace `https://fixrr.online` with your desired URL.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project folder:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the footer section and update the placeholder links:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <!-- Update these href attributes -->
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match link hrefs
   - Check for typos in IDs
   - IDs should not contain spaces

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the responsive class structure:
     ```html
     class="text-4xl md:text-5xl lg:text-6xl"
     ```

3. **Animation Problems**
   - Check if AOS script is loaded
   - Verify data-aos attributes are spelled correctly:
     ```html
     data-aos="fade-up"
     data-aos-delay="100"
     ```

### Need Help?
- Double-check your changes against the original code
- Use browser developer tools (F12) to inspect elements
- Ensure all HTML tags are properly closed
- Maintain the existing indentation for readability

Remember to test all changes across different screen sizes and browsers before deploying to production.