# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the IDO Consulting landing page. Follow these step-by-step instructions to make common updates while preserving the page's responsive design and functionality.

## 1. Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold">IDO Consulting</a>
```
To update the company name:
1. Locate this line in the header section
2. Replace "IDO Consulting" with your desired text
3. Maintain the surrounding HTML tags

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">Transform Your Organization with Strategic Guidance</h1>
<p class="text-xl md:text-2xl text-gray-600">{hero_statement}</p>
```
To update the main headline and hero statement:
1. Replace the h1 text between the tags
2. Replace `{hero_statement}` with your actual hero text
3. Keep the class attributes unchanged to maintain responsive sizing

### Tailwind CSS Class Modifications

#### Understanding Key Classes
- `container mx-auto`: Centers content with automatic margins
- `px-6`: Adds horizontal padding (left and right)
- `py-4`: Adds vertical padding (top and bottom)
- `md:`: Applies styles only on medium-sized screens and larger
- `text-gray-600`: Sets text color to a medium gray
- `hover:`: Applies styles when elements are hovered over

#### Modifying Colors
To change the gradient colors in the header:
```html
<!-- Original -->
<a class="bg-gradient-to-r from-blue-600 to-purple-600">

<!-- Example modification -->
<a class="bg-gradient-to-r from-green-600 to-blue-600">
```

#### Responsive Design Tips
- Keep the `md:` and `lg:` prefixes when modifying classes
- Maintain the responsive grid structure in features and benefits sections
- Test all changes across different screen sizes

## 2. Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

To update navigation links:
1. Locate the `href` attributes
2. For internal sections, use `#section-id`
3. For external links, use complete URLs
4. Example: `<a href="https://example.com/features">Features</a>`

### Call-to-Action Links
```html
<!-- Main CTA button -->
<a href="https://idoconsulting.ca" class="inline-block px-8 py-4">
```
To update:
1. Replace `https://idoconsulting.ca` with your desired URL
2. Ensure the URL includes `https://` or `http://`
3. Test the link after updating

### Email Links
```html
<a href="mailto:js@idoconsulting.ca">
```
To update:
1. Replace `js@idoconsulting.ca` with your email address
2. Keep the `mailto:` prefix
3. Test the email link functionality

## 3. Linking Privacy and Terms Pages

### Footer Link Updates
Current footer structure:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

### Troubleshooting Tips
- Verify all file names match exactly (case-sensitive)
- Ensure privacy and terms pages are in the correct directory
- Test links in multiple browsers
- Check that styling matches existing links

## Common Issues and Solutions

1. **Broken Internal Links**
   - Verify that section IDs match the href attributes
   - Check for typos in IDs and href values
   - Ensure sections have unique IDs

2. **Responsive Design Issues**
   - Don't remove responsive classes (md:, lg:)
   - Test on multiple screen sizes
   - Use browser developer tools to check breakpoints

3. **Gradient Colors Not Showing**
   - Verify Tailwind CSS is properly loaded
   - Check class name spelling
   - Ensure color values are valid Tailwind colors

Remember to:
- Back up files before making changes
- Test all modifications in multiple browsers
- Validate HTML after making changes
- Keep consistent styling across all pages

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.