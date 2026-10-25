## 8. Reference-Driven Visual Design System and Layout Exploration

### Objective

I will provide additional reference images collected from different apps, websites, and digital products. Use these references to develop a distinctive, sophisticated visual design system for Leafora.

The references are intentional design inputs, not images to copy blindly. Analyse their visual characteristics and determine which design principles, interface patterns, image treatments, and layout techniques can improve our application.

Do not assume that every reference uses the same style or that every style should appear on every screen.

### A. Analyse every reference

For each supplied reference image, identify:

- Overall design style and visual character.
- Colour palette, colour relationships, and gradient treatment.
- Typography, hierarchy, and whitespace.
- Image composition, cropping, aspect ratios, and visual balance.
- Product-card layouts and product-image presentation.
- Background treatments, borders, shadows, transparency, and depth.
- Use of glassmorphism, editorial layouts, asymmetric grids, layered compositions, or other relevant techniques.
- Navigation, controls, content organisation, and interaction patterns.
- What makes the design effective and what would or would not translate to Leafora.

Extract reusable design principles instead of copying another brand's identity.

### B. Explore multiple design techniques selectively

Evaluate the following techniques against the references and the actual needs of each screen:

**1. Glassmorphism**

Use translucent surfaces, subtle backdrop blur, restrained borders, and layered depth where they improve hierarchy or create an elegant floating interface.

Potential applications:
- Floating search and filter panels.
- Promotional overlays on suitable lifestyle imagery.
- Contextual controls over image backgrounds.
- Selected navigation or floating utility elements.

Do not make every card translucent. Maintain readable contrast, accessible controls, and suitable performance on supported devices.

**2. Editorial botanical design**

Use generous whitespace, elegant typography, strong photography, intentional asymmetry, and considered compositions to communicate a premium botanical brand.

Potential applications:
- Homepage hero sections.
- Featured plant collections.
- Editorial plant-care content.
- Seasonal collections and curated bundles.

**3. Clean product-commerce layouts**

Use clear product photography, readable product names, prices, care attributes, and purchase actions.

Potential applications:
- Standard product listings.
- Product comparison and filtering.
- Product details and variant selection.
- Cart and checkout.

**4. Structured and asymmetric product grids**

Explore different grid arrangements where useful, including standard grids, featured-product layouts, editorial mosaics, horizontal carousels, and mixed image sizes.

Use these patterns to create visual interest without sacrificing product discoverability, comparison, responsiveness, or consistency.

**5. Layered and immersive imagery**

Consider full-bleed photography, image-led banners, overlapping content panels, carefully controlled colour surfaces, and lifestyle compositions when supported by the references.

Keep text legible and ensure that product information remains easy to find.

These are candidate techniques, not mandatory styles. Use others if the supplied references justify them.

### C. Use category-specific product presentation

Do not force every plant category into an identical product-card layout.

Choose presentation patterns according to the product's characteristics and the customer's shopping task.

Examples to evaluate:

- **Statement and large indoor plants:** Larger photography, visible overall plant shape, height information, and suitable-space context.
- **Small plants and succulents:** Compact grids that support browsing and comparison, with clear plant names and prices.
- **Flowering plants:** Photography that makes genuine flowers, colour, and seasonal characteristics easy to understand.
- **Herbs and edible plants:** Practical care attributes, growing requirements, and relevant indoor or outdoor context.
- **Trees and outdoor plants:** Appropriate scale, growth information where verified, and garden or outdoor context.
- **Pots and accessories:** Clean product-focused imagery, material and size information, and clear compatibility with plants.
- **Curated bundles:** Group compositions showing the included products, sizes, individual items, bundle price, and genuine savings.
- **Plants for specific spaces:** Lifestyle imagery showing plants in relevant settings, such as offices, living rooms, balconies, or gardens.
- **Plant-care services:** Service-led layouts that explain the offering, inclusions, eligibility, pricing, and booking action.

These are starting points for design evaluation, not fixed layouts. Adapt them based on the references, the real catalogue, and usability requirements.

### D. Create a reusable layout-pattern library

Before implementing many variations, identify a small, purposeful set of reusable patterns, such as:

- Standard product card.
- Featured product card.
- Editorial product tile.
- Compact horizontal product row.
- Category hero.
- Collection banner.
- Bundle composition card.
- Lifestyle image with text overlay.
- Product detail gallery.
- Product recommendation section.

Document when each pattern should be used, its image requirements, responsive behaviour, and accessibility considerations.

Reuse components where their behaviour and structure are genuinely shared. Support variants through explicit component properties or design tokens rather than duplicating inconsistent styles across the application.

### E. Preserve one coherent Leafora identity

Visual variety must not create a fragmented website.

Keep typography, spacing, core colours, interaction states, navigation, buttons, and key product information consistent.

Different categories may use different image ratios, compositions, and card arrangements, but they must still feel like parts of the same brand.

Avoid excessive gradients, unnecessary glass effects, heavy shadows, random corner radii, decorative animation, and competing visual treatments.

### F. Reference approval and implementation

1. Review the reference images I provide.
2. Map each reference to its useful design principles and potential application within Leafora.
3. Propose a concise visual direction and category-to-layout mapping.
4. Identify the highest-impact changes to the current implementation.
5. Implement the approved direction using the existing project architecture.
6. Verify the result across desktop, tablet, and mobile.

Do not wait for references that have not yet been supplied. Audit the existing application and prepare the implementation plan first, but do not make major subjective redesign decisions based on imagined references.

Use reference images to inform the interface, not as permission to reuse copyrighted assets. Product photography must still meet the image-sourcing requirements in `IMAGE_ASSET_REGISTER_V1.md`.

### Acceptance criteria

- The supplied references visibly inform the design decisions.
- Each product category uses an appropriate, purposeful presentation.
- Glassmorphism and other visual techniques are used selectively.
- The product catalogue remains easy to browse and compare.
- Shared components remain consistent and maintainable.
- The responsive experience preserves the intended hierarchy.
- Every visual treatment supports the customer experience rather than serving as decoration alone.
