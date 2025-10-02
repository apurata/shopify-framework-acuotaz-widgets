# Acuotaz Shopify Widgets

This Shopify app provides theme extension widgets for integrating Acuotaz payment solutions into your Shopify store.

## Overview

The Acuotaz Shopify Widgets app provides three customizable widgets that integrate seamlessly with your Shopify theme:

- **Acuotaz Headband**: Displays payment information banner at the top of your store
- **Acuotaz Addon**: Shows payment options on product pages based on product price
- **Payment Mocker**: Mockup widget for payment information display

## Installation

### For Shopify Store Owners

1. **Install from Shopify App Store**:
   - Go to your Shopify Admin
   - Navigate to Apps → App Store
   - Search for "Acuotaz Widgets"
   - Click "Install app"

2. **Add widgets to your theme**:
   - Go to Online Store → Themes
   - Click "Customize" on your active theme
   - Navigate to the section where you want to add the widget
   - Click "Add block" → "Acuotaz Widgets"
   - Choose the widget you want to add

3. **Configure Client ID**:
   - In the widget settings, enter your Acuotaz Client ID
   - Save changes
   - The widget will automatically load payment information

### Widget Placement

#### 1. Acuotaz Headband
Add to your theme header for maximum visibility:

**Recommended placement**: Header section
- Displays payment information banner
- Shows across all pages
- Responsive design

#### 2. Acuotaz Addon
Add to product pages for payment options:

**Recommended placement**: Product page, after price
- Automatically detects product price
- Shows payment options based on price
- Updates when product variants change

#### 3. Payment Mocker
Add anywhere for payment information display:

**Recommended placement**: Any section
- Configurable mockup widget
- Useful for testing and demonstrations

## For Developers

### Development Setup

1. **Clone the repository**:
```bash
git clone <repository-url>
cd apurata-widgets
```

2. **Install dependencies**:
```bash
npm install
```

3. **Start development server**:
```bash
npm run shopify app dev
```

4. **Configure Client ID** in each widget's settings

### Technical Details

- **API Endpoints**:
  - Headband: `https://apurata.com/pos/info-steps`
  - Addon: `https://apurata.com/pos/pay-with-apurata-add-on`
  - Payment Mocker: `https://apurata.com/pos/info-steps`

- **Variant Change Optimization**: Smart detection prevents unnecessary API calls
- **Error Handling**: Graceful fallback for API failures
- **Responsive Design**: Works on all device sizes

## Support

For support, please contact:
- **Email**: andy@apurata.com
- **Website**: https://apurata.com

