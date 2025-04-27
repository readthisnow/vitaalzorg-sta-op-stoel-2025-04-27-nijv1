# Vitaalzorg Landing Page Maintenance Guide

This guide will help you maintain and customize the Vitaalzorg landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Company Name/Logo**
```html
<a href="/" class="text-2xl font-bold text-gray-800">
    Vitaalzorg  <!-- Change this text to update company name -->
</a>
```

2. **Navigation Menu Items**
```html
<div class="hidden lg:flex space-x-8">
    <a href="#features">Kenmerken</a>  <!-- Update these text labels -->
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Vitaalzorg Sta Op Stoel  <!-- Update main headline here -->
</h1>
<p class="text-xl sm:text-2xl text-gray-600 mb-8">
    Tijdelijk 10% Korting | Optimaal Comfort & Mobiliteit  <!-- Update subheadline -->
</p>
```

#### Understanding Tailwind Classes
- `text-4xl`: Large text size (mobile)
- `sm:text-5xl`: Larger text on small screens
- `lg:text-6xl`: Largest text on large screens
- `mb-6`: Margin bottom spacing
- `text-gray-900`: Dark gray text color

### Modifying Button Styles
```html
<a href="https://sta-opstoelen.nl" class="inline-flex items-center justify-center px-8 py-4 text-lg font-semibold text-white bg-blue-600 rounded-full hover:bg-blue-700">
```

To change button colors:
1. Replace `bg-blue-600` with any color (e.g., `bg-red-600`)
2. Update hover state `hover:bg-blue-700` to match
3. Common colors: `blue`, `red`, `green`, `yellow`, `purple`

## Managing Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Kenmerken</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://sta-opstoelen.nl">Bekijk Aanbod</a>
<a href="#contact">Gratis Advies</a>
```

### Updating Links
To update any link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. For internal sections, use `#section-name`
4. For external links, use full URL starting with `https://`

Example:
```html
<!-- Before -->
<a href="https://sta-opstoelen.nl">

<!-- After -->
<a href="https://your-new-url.com">
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

```html
<footer class="bg-gray-900 text-gray-300 py-12">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
            <!-- Add this section -->
            <div class="space-y-4">
                <h3 class="text-lg font-semibold">Legal</h3>
                <ul class="space-y-2">
                    <li>
                        <a href="/privacy.html" class="hover:text-white transition-colors duration-300">
                            Privacy Policy
                        </a>
                    </li>
                    <li>
                        <a href="/terms.html" class="hover:text-white transition-colors duration-300">
                            Terms of Service
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</footer>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Use same header/footer as main page
3. Add content between `<main>` tags
4. Maintain consistent styling

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Check that section IDs match href attributes
- Ensure no spaces in IDs
- IDs should be lowercase

2. **Responsive Design Issues**
- Check mobile view using browser dev tools
- Verify Tailwind breakpoint classes:
  - `sm:` (640px)
  - `md:` (768px)
  - `lg:` (1024px)

3. **Button Styling Problems**
- Confirm all utility classes are spelled correctly
- Check for conflicting classes
- Ensure proper class order for hover states

### Need Help?
- Check [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always test changes across different devices and browsers before deploying to production.