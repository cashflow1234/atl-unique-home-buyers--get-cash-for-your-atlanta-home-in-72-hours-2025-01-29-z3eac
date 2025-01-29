# ATL Home Buyers Landing Page - Maintenance Guide

This guide will help you maintain and customize the ATL Home Buyers landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and main call-to-action button:
```html
<div class="text-2xl font-bold text-blue-600">ATL Home Buyers</div>
```
To change the logo text:
1. Locate this div in the header section
2. Replace "ATL Home Buyers" with your desired text
3. Adjust size using these Tailwind classes:
   - `text-2xl` (current size)
   - `text-xl` (smaller)
   - `text-3xl` (larger)

### Hero Section
The main headline and subtext are in the hero section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8 leading-tight">
    Get Cash For Your Atlanta Home In 72 Hours
</h1>
```
To modify:
1. Change the text between the `<h1>` tags
2. Maintain the responsive sizing classes:
   - `text-4xl` (mobile)
   - `md:text-5xl` (tablet)
   - `lg:text-6xl` (desktop)

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition duration-300">
    <h3 class="text-xl font-semibold mb-4 text-gray-900">Feature Title</h3>
    <p class="text-gray-600">Feature description text here.</p>
</div>
```
To add/modify features:
1. Copy the entire `div` block
2. Change the title in the `<h3>` tag
3. Update the description in the `<p>` tag
4. Maintain the styling classes for consistency

## Managing Links

### Current Links
The page contains these important links:
1. Cash Offer Form:
```html
<a href="https://form.jotform.com/250276622130043" class="inline-block px-8 py-4 bg-blue-600">
```
2. Email Contact:
```html
<a href="mailto:getoffer@atlfastcash.com" class="text-white hover:text-blue-100">
```

To update links:
1. Locate the `<a>` tag
2. Change the `href` attribute value
3. Example:
```html
<a href="YOUR-NEW-LINK-HERE" class="[existing-classes]">
```

### Link Styling
All links use these common styles:
- Primary buttons: `bg-blue-600 text-white rounded-full`
- Secondary links: `text-white hover:text-blue-100`

## Adding Privacy and Terms Pages

Add privacy and terms links to the footer:
```html
<!-- Footer -->
<footer class="bg-gray-900 text-gray-300 py-12">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center">
            <p class="text-sm">&copy; 2024 ATL Home Buyers. All rights reserved.</p>
            <!-- Add these lines below the copyright notice -->
            <div class="mt-4 space-x-4">
                <a href="privacy.html" class="text-sm hover:text-white">Privacy Policy</a>
                <a href="terms.html" class="text-sm hover:text-white">Terms of Service</a>
            </div>
        </div>
    </div>
</footer>
```

## Troubleshooting

Common issues and solutions:

### Text Not Wrapping Correctly
If text overflows its container:
1. Add `whitespace-normal` class
2. Ensure proper responsive classes are used
3. Check container width classes (`max-w-*`)

### Buttons Not Aligned
If buttons are misaligned:
1. Verify `flex` classes on parent container
2. Check for proper spacing classes (`gap-*`, `space-x-*`)
3. Ensure consistent padding classes (`px-*`, `py-*`)

### Mobile Responsiveness Issues
If layout breaks on mobile:
1. Check for responsive prefixes (`sm:`, `md:`, `lg:`)
2. Verify grid column classes (`grid-cols-1 md:grid-cols-3`)
3. Test different screen sizes using browser developer tools

### Color Consistency
To maintain brand colors:
1. Use existing color classes (`blue-600`, `gray-900`)
2. Keep hover states consistent (`hover:bg-blue-700`)
3. Match text colors with their sections (`text-gray-900`, `text-white`)

Remember to:
- Always test changes across different screen sizes
- Maintain consistent spacing and padding
- Keep the responsive design intact
- Back up files before making changes

Need more help? Contact your web developer or refer to [Tailwind CSS documentation](https://tailwindcss.com/docs).