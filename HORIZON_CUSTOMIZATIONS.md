# Horizon Labs Marketplace Customizations

This document tracks all customizations made to the Sharetribe web-template for Horizon Labs.

## Changes Made

### 1. Marketplace Name
**File**: `src/config/configDefault.js`
**Change**: Updated marketplace name from `[Marketplace Name]` to `Horizon Labs Marketplace`
**Line**: `marketplaceName: process.env.REACT_APP_MARKETPLACE_NAME || 'Horizon Labs Marketplace'`

### 2. Primary Brand Color
**File**: `src/config/configBranding.js`
**Change**: Updated primary marketplace color from `#7c3aed` to `#1a1a2e`
**Line**: `export const marketplaceColor = '#1a1a2e';`

### 3. Logo Replacement
**Files Created**:
- `src/assets/horizon-labs-logo-desktop.svg` - Desktop logo with full "Horizon Labs" text
- `src/assets/horizon-labs-logo-mobile.svg` - Mobile logo with "Horizon" text

**File Modified**: `src/config/configBranding.js`
**Changes**:
- Updated desktop logo import: `import logoImageDesktop from '../assets/horizon-labs-logo-desktop.svg';`
- Updated mobile logo import: `import logoImageMobile from '../assets/horizon-labs-logo-mobile.svg';`

### 4. Logo Design Details
**Desktop Logo SVG** (`horizon-labs-logo-desktop.svg`):
```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 200 50">
  <text x="10" y="35" font-size="24" font-family="sans-serif" fill="#1a1a2e" font-weight="bold">Horizon Labs</text>
</svg>
```

**Mobile Logo SVG** (`horizon-labs-logo-mobile.svg`):
```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 150 40">
  <text x="10" y="28" font-size="20" font-family="sans-serif" fill="#1a1a2e" font-weight="bold">Horizon</text>
</svg>
```

## Branding Guidelines

### Color Palette
- **Primary Color**: `#1a1a2e` (Dark navy blue)
- **Generated Colors**:
  - `--marketplaceColorDark`: 10% darker than primary (auto-generated)
  - `--marketplaceColorLight`: 10% lighter than primary (auto-generated)

### Typography
- **Logo Font**: Sans-serif, bold weight
- **Desktop Logo**: 24px font size
- **Mobile Logo**: 20px font size

### Logo Usage
- **Desktop**: Full "Horizon Labs" text
- **Mobile**: Shortened to "Horizon" for space constraints
- **Color**: Uses primary brand color (#1a1a2e)

## Files Not Modified

The following files were intentionally left unchanged as per requirements:
- Payment configuration files
- Listing types configuration
- Transaction flow configuration
- Any backend or API-related files

## Next Steps for Production

1. **Brand Assets**: Replace SVG text logos with actual Horizon Labs logo files when available
2. **Color Refinement**: Update color palette if official Horizon Labs brand colors differ from `#1a1a2e`
3. **Social Media Images**: Replace placeholder social sharing images with Horizon Labs branded versions
4. **Brand Image**: Replace the hero section background image with Horizon Labs branded imagery

## Deployment Notes

- All changes are in the `feature/horizon-branding` branch
- No breaking changes to existing functionality
- Branding changes are purely visual and don't affect core marketplace functionality
- SVG logos ensure crisp rendering at any resolution