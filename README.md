# Miami Home Loans Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Miami Home Loans landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Legal Pages](#adding-legal-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To modify:

1. **Logo Text**
```html
<!-- Find this section in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">MHL</a>
```
- Replace "MHL" with your desired logo text
- Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)
- Change color using `text-blue-600` (options: text-red-600, text-green-600, etc.)

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Best Mortgage Broker In Miami
</h1>
```
- Replace the heading text while maintaining the HTML structure
- Adjust responsive text sizes:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Features Section
To modify service cards:

```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-home text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">First Home Buyer</h3>
    <p class="text-gray-600 leading-relaxed">
        Specialized guidance and support for first-time homebuyers
    </p>
</div>
```
- Update icon: Change `fa-home` to any [Font Awesome](https://fontawesome.com/icons) icon
- Modify heading: Replace "First Home Buyer" text
- Update description: Modify the paragraph text
- Maintain the class structure for consistent styling

## Managing Links

### Navigation Menu Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```
To update:
1. Locate the `href` attribute
2. For internal links (same page):
   - Use `#section-id` format
   - Ensure the referenced section has matching ID
3. For external links:
   - Replace with full URL (e.g., `href="https://example.com"`)

### Call-to-Action Links
```html
<a href="mailto:admin@mhl.com" class="inline-block bg-white text-blue-600 px-8 py-4 rounded-full">
    Contact Us Now
</a>
```
- Update email address in `mailto:` link
- Maintain the class structure for styling
- Test links after updating

## Adding Legal Pages

### Footer Legal Links
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-6">Legal</h4>
    <ul class="space-y-4">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Disclaimer</a></li>
    </ul>
</div>
```
To link legal pages:
1. Create your legal page files (e.g., `privacy.html`, `terms.html`)
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match exactly with href values
- Section IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
- Maintain responsive class prefixes:
  - `md:` for tablet breakpoint
  - `lg:` for desktop breakpoint
- Don't remove display classes like `hidden md:flex`

3. **Icon Not Showing**
- Verify Font Awesome is properly loaded in header
- Check icon class names against Font Awesome documentation
- Ensure proper icon prefix (fas, fab, far)

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check [Font Awesome](https://fontawesome.com/icons) for icon references
- Test all changes in multiple browsers and device sizes

Remember to:
- Back up files before making changes
- Test all modifications in a development environment
- Validate links and functionality after updates
- Maintain consistent styling across all pages