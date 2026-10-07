# Corner & Co. — Local Shop Product Catalogue

A responsive, local-first e-commerce mini project for a neighborhood shop. Customers can browse and filter products, manage a persistent bag, complete a simulated checkout, and print their receipt. A lightweight shop management page lets an administrator maintain the catalogue and order statuses.

## Features

- Home, catalogue, product details, bag, checkout, order confirmation, about, contact, and shop admin views.
- 22 sample products in seven categories, with ratings, stock, descriptions, sale prices, and product photos.
- Live search, category, price, rating, stock and sale filters, sorting, and clear filters.
- Stock-aware quantity controls and a bag that persists across refreshes.
- Validated checkout, generated order IDs, saved orders, inventory deduction, and printable receipts.
- Admin product add/edit/delete, stock changes, and order status management.
- Responsive mobile navigation, keyboard focus styles, accessible labels, empty states, and toast messages.

## Technologies

Semantic HTML5, CSS3, and plain JavaScript. Browser LocalStorage is the persistence layer; no database, build step, or paid API is required. Product photography loads from Unsplash and Google Fonts are used for typography. The app includes a graceful fallback image when a photo URL fails.

## Folder structure

```text
local-shop-catalogue/
├── index.html       # App shell and shared navigation/footer
├── styles.css       # Responsive styles and print receipt styles
├── app.js           # Sample data, routes, catalogue, cart, checkout and admin logic
└── README.md
```

## How to run

Open `index.html` in a modern browser. For the most consistent browser behavior, serve the folder with any static HTTP server, for example:

```sh
python -m http.server 8000
```

Then visit `http://localhost:8000`. There is no compilation or package installation step.

## How LocalStorage works

On first launch, the app saves its sample catalogue under `corner-products-v1`. The bag, orders, and most recent order use `corner-cart-v1`, `corner-orders-v1`, and `corner-last-order-v1`. Values are JSON, persist in the current browser profile, and can be reset by clearing this site's LocalStorage. Checkout deducts stock and records an order in the browser. This is a simulated shop: there is no real payment processing or shared server database.

## Shop admin

Choose **Shop admin** in the navigation. Add, edit, and delete products, update stock, and change order statuses. Admin changes are saved in the same LocalStorage catalogue that the customer pages read. This demo page has no authentication and is intended for a college project running locally.

## Mini Project Objectives

This project demonstrates modern web programming concepts through semantic HTML, responsive CSS, client-side routing, dynamic DOM rendering, event handling, search and sorting, form validation, reusable data-driven UI, browser storage, error handling, and accessible interaction patterns. It connects the full shopping flow—from catalogue discovery through order placement—with a local admin workflow.

## Future enhancements

Connect a server and database for shared inventory, add admin authentication and real payment integration, and introduce order tracking and a live map service.
