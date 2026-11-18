# PERCENT — Concept Storefront V2

Standalone HTML, CSS and JavaScript storefront. V2 preserves the approved V1 design, gradient palette, concept imagery and two signature T-shirt fits. No install, dependencies, CDN, API keys or internet connection required. This is not yet a Shopify theme.

## Open and test

Extract the entire archive and open `percent-frontend-v2/index.html` in a recent browser. For the best experience use VS Code Live Server or run `python -m http.server 8000` in the extracted folder and open `http://localhost:8000`. Do not open the HTML inside the compressed archive.

## V2 improvements

- Homepage Hero, Latest Drop, Try the Look and Best Sellers are navigable by gesture rather than arrow buttons. Latest Drop and Try the Look move with the pointer/finger, have momentum and snap to a centered item. The dots are passive position indicators. Keyboard left/right controls remain; Enter opens the focused product. Horizontal trackpad wheel input is supported on the garment and look rails.
- Tap any garment on the Latest Drop rail, any model in Try the Look, a product card, a lookbook hotspot or a product link to open an animated product details overlay. On mobile the overlay is full-screen; on desktop it appears as a large modal. It has its own scrolling area and a fixed close header. The underlying page stays mounted, preserving its carousel selection and vertical scroll. Close with ×, Escape or (desktop) the backdrop. Dragging does not trigger a product tap. Direct #product links still resolve to a standalone page.
- Product variants, size guide, quantity, recommendations and cart actions are still available. Size guide and cart are nested drawers; closing them returns to the product overlay.
- Dummy My Profile page, reachable from the mobile menu, desktop profile icon or footer. Account details, My Orders and Addresses are local demo views. No actual login, order history or personal information collection.
- V1 cart storage key is retained for compatibility. Cart and checkout remain simulated.

## Manual acceptance checklist

1. On a phone, swipe Latest Drop across several colorways in both directions. Confirm garments follow your finger and snap; vertical page scrolling remains natural.
2. Swipe Try the Look, Best Sellers and hero. Check that the active look and text stay synchronized and no arrows appear on the homepage.
3. Tap a noncenter or center garment. Confirm correct product opens. Select color and size, open and close the size guide, add to bag, then close the bag and product overlay. Check that your original viewport and carousel position are restored.
4. Test opening another product from recommendations within the modal; close and return to the original homepage. Check Escape and desktop backdrop close.
5. Open My Profile from the mobile menu. Test Account, My Orders, Addresses and View Bag. Confirm no real data is requested.
6. Test search, fit filters, cart quantities, keyboard navigation and reduced motion. Real-device frame timing is still to be assessed.

## 3D direction

The current imagery is preserved deliberately. Three.js does not supply a suitable branded garment or human model by itself; it renders imported models. No verified, matching commercially licensed GLB assets were provided. See `3D-INTEGRATION.md` for the proposed asset-based approach. V2 has no 3D engine or synthetic replacement meshes.

## Files

- `index.html`: global navigation, page container, modal shells.
- `styles.css`: design, responsive layouts and animation.
- `app.js`: catalog, gesture handling, product modal, hash routing, dummy profile and cart.
- `assets/`: concept-derived local imagery; not actual product photography.
- `TEST-RESULTS.txt`: completed checks and remaining limitations.

All product names, prices, artwork, sizes, inventory and policies are illustrative. No Shopify store, Horizon theme, production site, account or payment provider has been modified. Shopify integration remains a later phase.
