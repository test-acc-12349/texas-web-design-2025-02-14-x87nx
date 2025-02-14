# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu:
```html
<div class="text-2xl font-bold text-blue-600">TWD</div>
```
To change the logo text:
1. Locate this div in the header section
2. Replace "TWD" with your desired text
3. Adjust text size by changing `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

### Hero Section
The main headline and subheading are in the hero section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```
To modify:
1. Replace the text between the `<h1>` tags for the main headline
2. Replace the text between the `<p>` tags for the subheading
3. The classes `md:text-5xl` and `lg:text-6xl` control responsive text sizing

### Feature Cards
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-server text-4xl"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included with every website package.</p>
</div>
```
To update:
1. Change the icon by replacing `fa-server` with another [Font Awesome icon](https://fontawesome.com/icons)
2. Modify the heading text between the `<h3>` tags
3. Update the description between the `<p>` tags

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```
To update:
1. The `href="#features"` points to the section ID on the page
2. Ensure section IDs match these links (e.g., `id="features"`)
3. To link to external pages, replace `#features` with the full URL

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <i class="fab fa-twitter text-xl"></i>
    </a>
```
To update:
1. Replace `href="#"` with your social media profile URLs
2. Ensure all social links are active and correct
3. Test each link after updating

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these links to the Quick Links section in the footer:
```html
<ul class="space-y-2">
    <!-- Existing links -->
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match navigation href attributes
   - IDs must be unique and contain no spaces
   - Example: `href="#contact"` must match `id="contact"`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes
   - Test all changes on mobile, tablet, and desktop views

3. **Icon Problems**
   - Verify Font Awesome is properly loaded
   - Check icon class names against Font Awesome documentation
   - Use the correct icon prefix (`fas`, `fab`, etc.)

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to:
- Back up files before making changes
- Test all changes across different browsers
- Maintain consistent spacing and indentation
- Keep the original file structure intact