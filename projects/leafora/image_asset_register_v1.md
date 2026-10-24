## Image Sourcing, Visual Research & Product Presentation — V1

### 1. Objective

Create a consistent, premium botanical visual identity across the entire Leafora website. Every image must support the page's purpose, communicate useful information, and contribute to customer trust.

Do not select images randomly or use unrelated stock photos simply to fill empty spaces.

### 2. Visual inspiration and research sources

Use these sources to research visual direction, photography styles, product presentation, compositions, and design ideas:

- **Pinterest:** https://www.pinterest.com/ — botanical mood boards, plant styling, interior greenery, garden arrangements, product photography concepts, and visual composition.
- **Unsplash:** https://unsplash.com/ — botanical photography and lifestyle imagery, subject to the applicable license.
- **Pexels:** https://www.pexels.com/ — plant photography, interiors, gardens, and lifestyle imagery, subject to the applicable license.
- **Plant and nursery websites:** Research real plant retailers, nurseries, growers, and manufacturers for product photography, botanical details, sizes, product variants, and care information.
- **Premium interior and garden websites:** Research how plants are styled in living rooms, offices, balconies, rooftops, gardens, and other spaces.

Pinterest and other websites are primarily references for visual research. Do not assume an image is available for commercial reuse merely because it appears online. Obtain permission or use a suitable license when required. Review Pinterest's [copyright guidance](https://help.pinterest.com/en/article/copyright), the [Unsplash License](https://unsplash.com/license), and the [Pexels License](https://www.pexels.com/legal-pages/license/).

### 3. Image-source priority

Choose imagery in this order, depending on its purpose:

1. **Actual product photography:** Use approved photographs supplied by Leafora, the relevant seller, nursery, or manufacturer when available.
2. **Licensed botanical photography:** Use appropriately licensed images for lifestyle scenes, editorial content, and general inspiration.
3. **AI-generated concept imagery:** Use for original art direction, mood boards, and portfolio demonstrations where real product assets are unavailable. Clearly distinguish concept imagery from genuine product photographs.
4. **Temporary placeholders:** Use only during development, clearly identify them as placeholders, and replace them before the relevant experience is considered launch-ready.

Do not misrepresent a lifestyle photograph as an exact product, pot, size, colour, or bundle that Leafora actually sells.

### 4. Complete image inventory

Review every route and component in the application. Identify the image requirements for:

- Homepage hero and promotional banners.
- Shop-by-space and shop-by-plant-type categories.
- Product listing cards and product detail galleries.
- Plant size and product variants.
- Pots and compatible accessories.
- Curated bundles and customizable bundles.
- Wishlist, cart, and checkout summaries.
- Plant finder and recommendation results.
- Plant-care services and care-plan pages.
- Business and workplace greenery pages.
- Editorial articles and plant-care guides.
- Customer reviews and customer-uploaded photographs.
- Empty states, unavailable products, and other supporting UI states where imagery adds value.

Do not add decorative imagery to every state automatically. Use it when it improves understanding or supports the experience.

### 5. Product photography and display standards

Product images must be consistent enough to create a coherent shopping experience.

- Use clear, high-quality photographs with suitable crops and consistent presentation within each product category.
- Show the whole plant and its overall shape in the primary product image whenever practical.
- Use additional images for useful details, such as leaves, flowers, pot options, scale, and the plant styled in a real environment.
- Keep the plant visually prominent. Avoid busy backgrounds that compete with the product.
- Use lifestyle photographs to demonstrate how plants may look in real spaces, but keep lifestyle scenes distinct from exact product photography.
- Represent plant sizes and growth stages accurately. Do not imply that a small plant is a large mature specimen.
- Do not present a pot as included when it is an optional purchase.
- Keep product imagery consistent across product cards, product detail pages, cart, checkout, and order summaries.
- Where a seller offers multiple genuine variants, associate each variant with its correct approved image.
- Use suitable aspect ratios, responsive image sizes, descriptive alternative text, and optimised formats where supported.
- Provide graceful fallbacks for missing, broken, or unavailable images.

### 6. Visual research workflow

Before creating or selecting imagery for a major page:

1. Identify the page's purpose and the customer's information need.
2. Research relevant visual references from Pinterest and other appropriate websites.
3. Record the reference URL, what makes the composition effective, and which design principle can be adapted.
4. Determine whether the required asset should be actual product photography, licensed lifestyle photography, or AI-generated concept imagery.
5. Verify usage rights and relevant third-party restrictions before approving an asset.
6. Prepare an image specification covering subject, composition, background, lighting, crop, aspect ratio, and intended placement.
7. Check how the selected image works on desktop, tablet, and mobile.
8. Record the asset source, creator where available, licence or permission details, and any usage restrictions.

Use references to develop Leafora's own coherent art direction. Do not copy another retailer's entire visual identity, proprietary artwork, or protected images.

### 7. Asset organisation and tracking

Organise project assets clearly. Use an appropriate structure such as:

`public/images/`

- `brand/`
- `home/`
- `categories/`
- `products/`
- `pots/`
- `bundles/`
- `spaces/`
- `services/`
- `editorial/`
- `placeholders/`

Adapt this structure to the existing repository and framework rather than creating duplicate asset folders unnecessarily.

Maintain an image asset register, for example `docs/IMAGE_ASSET_REGISTER_V1.md`, documenting:

- Asset filename and intended use.
- Related page, product, or component.
- Source URL and creator, where known.
- Licence, permission, or seller approval.
- Whether the image is genuine product photography, licensed stock, AI-generated, or a temporary placeholder.
- Required attribution, restrictions, and replacement status.

### 8. Rules for Codex

- Inspect the existing repository and available assets before sourcing or generating new images.
- Inspect supplied design references where access is available; do not claim to have inspected inaccessible Figma files.
- Reuse suitable approved assets rather than generating unnecessary replacements.
- Do not hotlink arbitrary Pinterest images or unrelated retailer images into the application.
- Do not invent product images, seller approvals, product variants, or image licensing.
- Do not use AI-generated concept imagery as proof of a real product's appearance.
- If the correct image cannot be sourced, use an appropriate labelled placeholder and document what is missing.
- Do not block the entire shopping journey because a non-critical image is missing.
- Ensure images load reliably, crop correctly, and do not cause layout shifts or overflow.
- Keep the existing agreed Leafora design direction consistent across all pages.

### 9. Prototype versus commercial launch

**Prototype:** Licensed stock imagery and clearly identified AI-generated concepts may be used to demonstrate the intended experience. Fictional products and sellers must remain clearly identified as demo content.

**Commercial launch:** Product imagery must be accurate for the actual item being sold and appropriately authorised for use. Review every asset and its usage rights before launch.

### Acceptance criteria

- Every important image has a defined purpose and source.
- The asset register identifies provenance and usage status.
- Product imagery is consistent across listing, detail, cart, and checkout experiences.
- No image is presented as genuine product photography without adequate grounds.
- No image is approved for launch solely because it was found on Pinterest or another website.
- Responsive crops, loading behaviour, alternative text, and missing-image fallbacks are reviewed.
