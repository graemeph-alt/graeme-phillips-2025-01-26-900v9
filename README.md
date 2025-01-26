# Astrophotography Landing Page - Maintenance Guide

This guide will help you maintain and customize the Graeme Phillips Astrophotography landing page. Whether you're new to HTML and CSS or just getting started, follow these instructions to make updates while preserving the design integrity.

## 1. Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-8 tracking-tight">Graeme Phillips</h1>
<p class="text-xl md:text-2xl max-w-3xl mx-auto leading-relaxed text-gray-300 mb-12">
    I'm Graeme Phillips, an astrophotographer...
</p>
```
To update:
1. Locate the `<h1>` tag to change the main title
2. Find the paragraph `<p>` tag below to modify the introduction text
3. Keep the existing classes to maintain styling

#### Feature Cards
Look for three `<div>` elements under "What Drives Me" section:
```html
<div class="p-8 rounded-2xl bg-gray-800/50 backdrop-blur-lg hover:transform hover:scale-105 transition-all duration-300">
    <h3 class="text-xl font-semibold mb-4">Passion for the Night Sky</h3>
    <p class="text-gray-400">Dedicated to capturing...</p>
</div>
```
To update:
1. Locate each card's `<h3>` tag to change the title
2. Modify the `<p>` tag content for description
3. Maintain all classes for consistent styling

### Tailwind CSS Classes Explained

#### Common Classes Used:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-4`, `mb-8`)
- `bg-[color]`: Sets background color (e.g., `bg-black`, `bg-blue-600`)
- `hover:`: Adds hover effects (e.g., `hover:bg-blue-700`)

#### Responsive Design Classes:
```html
<div class="text-xl md:text-2xl">
```
- `md:`: Applies styles at medium screens (768px+)
- `lg:`: Applies styles at large screens (1024px+)

## 2. Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#about" class="hover:text-blue-400 transition-colors duration-300">About</a>
    <a href="#work" class="hover:text-blue-400 transition-colors duration-300">Work</a>
    <a href="#contact" class="hover:text-blue-400 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute in each `<a>` tag
2. Replace `#about` and `#work` with actual page sections (e.g., `#about-section`)
3. Ensure section IDs match in the HTML (add `id="about-section"` to corresponding sections)

### Email Link
```html
<a href="mailto:graeme@graemephillips.info" class="inline-block bg-blue-600...">
```
To update:
1. Replace `graeme@graemephillips.info` with your email address
2. Keep the existing classes for consistent button styling

## 3. Linking Privacy and Terms Pages

### Footer Links
Current footer structure:
```html
<div class="flex space-x-6">
    <a href="#" class="text-gray-500 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a>
    <a href="#" class="text-gray-500 hover:text-blue-400 transition-colors duration-300">Terms of Service</a>
</div>
```

To add proper links:
1. Create privacy.html and terms.html files in your project directory
2. Update the href attributes:
```html
<a href="privacy.html" class="text-gray-500 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-500 hover:text-blue-400 transition-colors duration-300">Terms of Service</a>
```

## Troubleshooting Tips

1. If styles aren't applying:
   - Check for typos in Tailwind class names
   - Ensure the Tailwind CSS CDN link is properly loaded
   - Verify class names match exactly (they're case-sensitive)

2. If links aren't working:
   - Confirm file names and paths are correct
   - Check that section IDs match href attributes exactly
   - Verify files exist in the correct directory

3. If responsive design isn't working:
   - Ensure viewport meta tag is present in head
   - Check media query prefixes (md:, lg:) are correctly placed
   - Test with browser dev tools in different screen sizes

## Best Practices

1. Always backup your files before making changes
2. Test all links after updating
3. View changes on multiple devices and browsers
4. Keep the same class structure when adding new elements
5. Maintain consistent spacing and indentation in your code

Need more help? Feel free to reference the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your web development team.