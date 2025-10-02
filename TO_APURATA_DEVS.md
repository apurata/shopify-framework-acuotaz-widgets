# Apurata Shopify Extension Widgets

## Overview
This Shopify extension provides three customizable widgets for Apurata payment integration:
- **Acuotaz Headband**: Displays payment information banner
- **Acuotaz Addon**: Shows payment options on product pages
- **Payment Mocker**: Mockup widget for payment information display

## Features Implemented

### ✅ Acuotaz Headband
- API correctly connected and positioned
- Displays payment information banner
- Responsive design with loading states
- Error handling for invalid tokens

### ✅ Acuotaz Addon
- **Product price recognition**: Automatically detects product prices
- **Variant change detection**: Optimized to reload only when product variants actually change
- **Smart loading**: Prevents unnecessary API calls when user selects the same variant multiple times
- **Error handling**: Graceful fallback for API failures

### ✅ Payment Mocker
- Mockup widget for payment information display
- Configurable client ID
- Loading and error states
- API integration with Apurata endpoints

## Technical Implementation

### Variant Change Optimization
The addon now uses intelligent variant detection:
```javascript
let currentVariantId = null;
document.addEventListener('change', function(e) {
  if (e.target.matches('input[name="id"], select[name="id"]')) {
    const newVariantId = e.target.value; // Selected variant ID (color, size, etc.)
    if (newVariantId !== currentVariantId) {
      currentVariantId = newVariantId;
      setTimeout(loadAddon, 100);
    }
  }
});
```

### API Endpoints
- **Headband**: `https://apurata.com/pos/info-steps`
- **Addon**: `https://apurata.com/pos/pay-with-apurata-add-on`
- **Payment Mocker**: `https://apurata.com/pos/info-steps`

## Installation & Configuration

### For Developers
1. Clone the repository
2. Install dependencies: `pnpm install`
3. Start development: `shopify app dev`
4. Configure client ID in each widget's settings

### For Merchants
1. Install the extension from Shopify App Store (when published)
2. Add widgets to theme sections
3. Configure Client ID in widget settings
4. Widgets will automatically appear on product pages

## Widget Configuration
Each widget requires a **Client ID** for API authentication:
- Go to widget settings
- Enter your Apurata Client ID
- Save changes
- Widget will automatically load payment information

## Status
- ✅ Headband API connected
- ✅ Addon price recognition working
- ✅ Payment Mocker implemented
- ⚠️ Headband not automatically placed on all views (requires manual theme integration)

