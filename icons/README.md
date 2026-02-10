# App Icons for PWA

This directory contains the app icons needed for your Progressive Web App. To properly set up your app icons, you need to generate them in the following sizes:

## Required Icon Sizes

- 72x72 pixels (icon-72x72.png)
- 96x96 pixels (icon-96x96.png)
- 128x128 pixels (icon-128x128.png)
- 144x144 pixels (icon-144x144.png)
- 152x152 pixels (icon-152x152.png)
- 192x192 pixels (icon-192x192.png)
- 384x384 pixels (icon-384x384.png)
- 512x512 pixels (icon-512x512.png)

## How to Generate Icons

### Option 1: Using PWA Asset Generator (Recommended)
```bash
npm install -g pwa-asset-generator
pwa-asset-generator logo.png ./icons --background "#0e0743" --splash-only --type png
```

### Option 2: Using an Online Tool
Visit: https://app-manifest.firebaseapp.com/ or https://www.pwa-manifest-generator.com/
- Upload your logo/icon (512x512 recommended)
- Select sizes needed
- Download all generated icons
- Place them in this directory

### Option 3: Manual Creation
Use image editing software like:
- Adobe Photoshop
- GIMP (Free)
- Figma
- Canva

Create your logo and resize it to all required dimensions.

## Icon Requirements

- Format: PNG (with transparency recommended)
- Background Color: #0e0743 (to match your app theme)
- Design: Should be recognizable at small sizes (72x72)
- Style: Consistent with your app brand

## File Naming Convention

Save files exactly as shown in the "Required Icon Sizes" section above.

## Maskable Icons

Modern PWAs support "maskable" icons which are displayed with different shapes on different platforms (rounded, teardrop, etc.). The manifest.json already includes the `purpose: "maskable"` property for these icons.

For best results:
- Leave 45% margin around your icon
- Design icons to use the full square (icon will be cropped to different shapes)
- Test how it looks with different shape masks

## Testing

After adding icons:
1. Open DevTools (F12)
2. Go to Application > Manifest
3. Verify all icons are loaded correctly
4. Check the "Add to Home Screen" preview

Your PWA is now ready to be installed on any device!
