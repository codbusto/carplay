# Tuttosconto - Idropulitrice Landing Page

## Shopify Integration Setup

To connect the order form to your Shopify store, you need to configure the following:

### 1. Shopify Storefront API Setup

1. Go to your Shopify Admin Panel
2. Navigate to Apps > Develop apps
3. Create a private app or use an existing one
4. Enable Storefront API access
5. Copy the Storefront access token

### 2. Product Configuration

1. In your Shopify admin, find the product variant ID for the idropulitrice
2. The variant ID should look like: `gid://shopify/ProductVariant/123456789`

### 3. Update OrderForm.tsx

Replace these values in `src/components/OrderForm.tsx`:

```javascript
const SHOPIFY_DOMAIN = 'your-shop-name.myshopify.com';
const STOREFRONT_ACCESS_TOKEN = 'your_storefront_access_token_here';

// In the lineItems array:
variantId: 'gid://shopify/ProductVariant/YOUR_VARIANT_ID'
```

### 4. Alternative: Webhook Integration

For a simpler setup, you can also use a webhook service like:
- Zapier
- Make.com (formerly Integromat)
- Custom webhook endpoint

This would send form data to your preferred system without requiring Shopify API credentials.

### Current Status

The form is currently set up to simulate successful orders. Once you configure the Shopify credentials above, it will create real checkouts in your Shopify store.

## Features

- Responsive design optimized for mobile and desktop
- Simplified order form with essential fields only
- Price: €65.00 per unit
- Quantity selection (1-5 units)
- Address collection for shipping
- Payment on delivery (COD)
- Free shipping in Italy

## Development

```bash
npm install
npm run dev
```

## Deployment

The site is deployed on Netlify and can be accessed at the provided URL.
