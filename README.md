# Little Smiles Pediatric Dental Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Little Smiles pediatric dental landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-blue-600">Little Smiles</a>
```
- Replace "Little Smiles" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)
- Change color using `text-blue-600` (options: text-red-600, text-green-600, etc.)

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight text-gray-900 mb-6">
    Pediatric Dental in Dallas, TX Near Me
</h1>
```
- Update heading text between the `<h1>` tags
- Responsive text sizes are defined as:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Services Cards
Each service card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Preventive Care</h3>
    <p class="text-gray-600">Regular check-ups and cleanings...</p>
</div>
```
To modify:
1. Change heading text between `<h3>` tags
2. Update description text between `<p>` tags
3. Adjust padding using `p-8` (options: p-4, p-6, p-12)

## Managing Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Internal page sections: Use `#section-name`
2. External pages: Use full URL (e.g., `https://example.com`)
3. Local pages: Use relative paths (e.g., `./about.html`)

### Appointment Button
Current appointment link:
```html
<a href="https://pediatric-dental-dallas-tx.netlify.app/" class="inline-block bg-blue-600 text-white text-lg px-8 py-4 rounded-full">
```
Replace the placeholder URL with your actual booking system URL.

## Adding Privacy and Terms Pages

### 1. Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### 2. Update Footer Links
Locate this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholders:
```html
<li><a href="./privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="./terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs
   - Verify that sections have the correct ID attribute

2. **Responsive Design Issues**
   - Check mobile-first classes (without prefix)
   - Verify breakpoint classes (md:, lg:)
   - Test on different screen sizes

3. **Style Inconsistencies**
   - Compare Tailwind classes with existing elements
   - Maintain consistent color schemes (blue-600, gray-900, etc.)
   - Keep consistent spacing patterns (px-6, py-4, etc.)

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Test changes using browser developer tools (F12)
- Make backups before significant changes
- Use version control if possible

Remember to test all changes across different devices and browsers to ensure consistency in appearance and functionality.