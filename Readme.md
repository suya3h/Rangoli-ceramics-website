# Rangoli Concepts

A responsive e-commerce website prototype for Rangoli Concepts, designed around the digital shopping experience for tiles, CP fittings, sanitaryware, wellness products, sinks, mirrors, adhesives, and related building products.

The project explores how a traditional showroom-oriented business could translate its product catalogue into a structured digital experience without losing the clarity of the physical buying process.

<img width="1920" height="873" alt="Rangoli" src="https://github.com/user-attachments/assets/9c2212e2-8910-4370-a134-3b9f52cc395f" />

## The problem

For a business with a large and varied physical catalogue, putting products online is not only a matter of displaying product cards.

Customers need to be able to quickly answer questions such as:

- What category does this product belong to?
- Which products match my requirements?
- What are the relevant specifications?
- Which brands are available?
- Can I narrow the catalogue down quickly?
- How do I move from browsing to enquiry?

A large catalogue without a useful information structure becomes difficult to browse, especially on mobile.

The goal of this prototype was therefore to treat the website as a product-discovery system rather than a collection of static product pages.

---

## Approach

The interface was designed around the idea of a digital catalogue that behaves more like a showroom.

The main flow is:

```text
Browse
  ↓
Search
  ↓
Filter
  ↓
Compare options
  ↓
Review product details
  ↓
Enquire / Add to cart
```

The catalogue is organized around categories and structured product attributes so that the same underlying information can support search, filtering, sorting, and product presentation.

The design also keeps the physical business context visible through showroom information, brand presentation, delivery messaging, product specifications, and enquiry-oriented interactions.

---

## What's implemented right now

### Product catalogue

The prototype contains a structured product catalogue with:

- Product categories
- Product cards
- Product specifications
- Brand information
- Pricing
- MRP display
- Product tags
- Availability states

Products are displayed through a reusable catalogue structure rather than individually designed pages.

### Search

The catalogue includes client-side product search designed around the way a customer might actually search for a product.

Examples include product names, product categories, and descriptive terms such as finishes or product types.

### Filtering

The catalogue includes filters for narrowing the available products based on structured attributes.

The interface keeps selected filters visible so that the current catalogue state remains understandable while browsing.

### Sorting

Products can be sorted through the catalogue toolbar, allowing the browsing experience to adapt to different shopping preferences.

### Cart and enquiry flow

The prototype includes cart-style interactions for:

- Adding products
- Removing products
- Adjusting quantities
- Calculating totals

The interface also includes enquiry-oriented states because a high-value showroom product does not always follow a conventional direct-checkout model.

### Account states

The prototype also explores guest and authenticated customer states, including account-related interface elements and sign-in interactions.

### Customer access and pricing

The catalogue intentionally changes depending on whether a customer is browsing as a guest or has logged in.

Before login, customers can:

- Browse products
- View product attributes and specifications
- Explore available product categories
- Explore product information
- See the available product brands

However, **product prices are not visible before login**.

After login, customers gain access to product pricing, but the brand information is no longer displayed.

This separation is intentional.

The idea is to allow customers to evaluate products based on their specifications and attributes before revealing commercial information, while removing the brand as a visible factor once pricing becomes available.

This helps reduce the possibility of the purchasing decision being influenced primarily by brand recognition and encourages comparison based on the actual product attributes and price.

The intended flow is:

```text
Guest
  ↓
Explore products
  ↓
Compare attributes / specifications / brands
  ↓
Login
  ↓
View pricing
  ↓
Evaluate products based on attributes + price
  ↓
Enquire / Add to cart
```

The prototype therefore treats authentication not only as an account feature, but as part of the product-discovery and purchasing experience.

### Responsive design

The catalogue was designed to adapt to different screen sizes.

On smaller screens:

- Navigation becomes compact
- Search moves into its own row
- Filters become easier to access
- Product cards adapt to narrower widths
- Multi-column sections collapse appropriately

The goal was to preserve the catalogue experience rather than simply shrinking the desktop layout.

---

## UX decisions

### Catalogue first

The main experience is built around discovering products rather than immediately pushing a single product or promotional message.

This is important for a showroom business where customers may arrive with a category requirement rather than a specific product name.

### Structured product information

Product cards expose information such as:

- Product name
- Manufacturer
- SKU
- Specifications
- Price
- Product size
- Tags

This allows the catalogue to function as a decision-making interface rather than only a visual gallery.

### Progressive interaction

The interface keeps the initial catalogue relatively simple, while filters, cart interactions, account states, and additional controls become available when they are relevant.

### Mobile-first considerations

The mobile layout is treated as a different interaction state rather than a smaller version of the desktop layout.

For example, the navigation, search, product grid, and catalogue controls change behavior at smaller breakpoints.

---

## Visual direction

The visual system was intentionally designed around the existing showroom and business context rather than a generic e-commerce template.

The interface uses:

- Warm neutral backgrounds
- Dark typography
- Gold and amber accents
- Serif display typography
- Compact product cards
- Structured spacing
- Strong catalogue hierarchy

The goal was to make the website feel appropriate for a business selling physical surfaces and bathroom products while keeping the interface practical enough for catalogue browsing.

---

## Iteration

This prototype was not treated as a one-pass implementation.

The interface went through multiple iterations while incorporating changing requirements and client input.

The iteration process was closer to:

```text
Initial direction
      ↓
Client input
      ↓
Layout changes
      ↓
UX refinement
      ↓
Interaction refinement
      ↓
Current version
```

The purpose of the iterations was not simply to change the visual design, but to improve how the catalogue, navigation, product discovery, and enquiry flow fit the underlying business.

---

## Technical implementation

The current prototype is implemented as a client-side website using:

### Frontend

- HTML5
- CSS3
- JavaScript

### Interface

- Responsive CSS Grid
- Flexbox
- CSS custom properties
- Responsive breakpoints
- Client-side interaction and state management
- Accessible focus states
- Reduced-motion support

The styling is written directly in CSS rather than relying on a component framework. The project uses a small design-token layer for typography, spacing, colors, and reusable interface patterns.

---

## What this prototype is

This is currently a **frontend prototype**, not a production e-commerce backend.

The purpose of the project is to explore:

- Information architecture
- Catalogue UX
- Product discovery
- Responsive behavior
- Interaction patterns
- Business-facing website structure

The current implementation does not include a production database, payment gateway, inventory system, or real authentication backend.

The product and account behavior is therefore designed to demonstrate the intended interface and user flow rather than represent a complete commerce platform.

---

## Why it is structured this way

The prototype deliberately keeps the frontend independent from backend infrastructure at this stage.

This allows the interface and user experience to be validated first before introducing:

- Product databases
- Inventory synchronization
- Customer accounts
- Order management
- Payment processing
- CRM integration

The current implementation therefore focuses on answering a simpler question first:

> Does the catalogue structure make sense for the customer and the business?

---

## Where this could go next

A production implementation could extend the existing interface with:

### Commerce

- Real product database
- Inventory synchronization
- Customer accounts
- Order management
- Checkout
- Payment integration

### Business systems

- ERP integration
- CRM integration
- Lead management
- Enquiry tracking
- Customer segmentation

### Product discovery

- Advanced filtering
- Product comparison
- Saved products
- Personalized recommendations
- Better search

### Operations

- Admin catalogue management
- Product approval workflows
- Pricing management
- Inventory availability
- Analytics

These are intentionally outside the scope of the current prototype.

---

## What I learned from the project

The main challenge was not writing the interface.

It was deciding what information should be visible, what should be interactive, and how much of the physical showroom experience should translate directly into the digital catalogue.

The project reinforced a simple principle:

```text
Good e-commerce UX is not only about displaying products.

It is about reducing the effort required to find
the right product and take the next action.
```

---

## Project status

**Status:** Frontend prototype

**Type:** E-commerce / Catalogue Experience

**Primary focus:**

- UI/UX
- Product discovery
- Responsive design
- Catalogue architecture
- Search and filtering
- Client-driven iteration

---

## Local usage

The project is currently a standalone HTML/CSS/JavaScript website.

Open the HTML file directly in a browser, or serve the project through any static web server.

---

## Deployment

The prototype can be deployed as a static website using services such as Netlify.

The current project does not require a backend to demonstrate the frontend experience.

---

## About the project

This project was developed as part of a broader exploration of business websites and e-commerce experiences for the building materials and sanitaryware industry.

The emphasis was on understanding the business, translating requirements into interface decisions, and iterating on the result rather than treating the website as a purely visual exercise.
