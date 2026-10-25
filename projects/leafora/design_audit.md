# LEAFORA — VISUAL QUALITY RESET AND UX DESIGN AUDIT

## Objective

The current Leafora implementation does not meet the intended design quality. It looks generic, visually plain, and insufficiently art-directed. Many AI-generated plant images look artificial, the colour gradients are not working harmoniously, and the result does not communicate the sophistication expected of a premium botanical e-commerce brand.

Do not respond by adding more gradients, shadows, decorative cards, animations, or random styling.

The objective is to improve the existing application through a structured UI/UX audit and evidence-based visual refinement.

## 1. Inspect before changing anything

Inspect:

- The existing application and all implemented routes.
- The current design tokens, CSS variables, typography, gradients, backgrounds, spacing, shadows, and component styles.
- Every currently used image and its source.
- The original Leafora Figma reference and the four supplied reference screens.
- `Leafora/LEAFORA_PROJECT_BRIEF_V1.md`
- `Leafora/IMAGE_ASSET_REGISTER_V1.md`

First report the five most important causes of the current visual weakness. Identify the exact components, styles, and assets responsible wherever possible.

Do not claim to have inspected a reference or source that you could not access.

## 2. Restore the intended art direction

The brand should feel premium, botanical, editorial, calm, confident, and commercially credible.

Develop a coherent visual system covering:

- A considered botanical colour palette with harmonious light and dark surfaces.
- Restrained, purposeful use of gradients rather than gradients applied indiscriminately.
- Elegant typography with a clear hierarchy between display headings, section headings, body text, prices, labels, and supporting information.
- Consistent spacing, alignment, content widths, image ratios, borders, radii, and shadows.
- Strong composition, whitespace, and visual balance.
- Accessible contrast and clear primary actions.

Do not invent exact design tokens supposedly extracted from Figma. Inspect the available reference first and document any values that cannot be verified.

## 3. Fix the product imagery

The current AI-generated images are not creating the required impression of authenticity.

Audit every image and classify it as:

- Genuine product photography.
- Licensed lifestyle or editorial photography.
- AI-generated concept imagery.
- Temporary placeholder.

Prioritise genuine, authorised product photographs for products customers could purchase. Use suitable licensed lifestyle photography for interiors, gardens, and aspirational scenes.

Use Pinterest and other retailers for visual research and composition references, not as permission to copy their images.

Do not fabricate product photography or present AI-generated plants as exact photographs of real stock. Do not silently substitute a different plant, pot, colour, or size.

If authentic product images are unavailable, document the missing assets and use clearly identified development placeholders until appropriate images are obtained.

Create a consistent image direction across the catalogue: believable lighting, natural plant detail, appropriate scale, clean composition, and consistent cropping.

## 4. Follow the original reference screens

Treat the supplied Figma screens as the primary visual reference.

Compare the current implementation against:

1. Home.
2. Product details.
3. Cart.
4. Onboarding.

Identify differences in layout, hierarchy, typography, colour relationships, imagery, spacing, and component treatment.

Preserve the important visual characteristics of the reference. Do not redesign these screens arbitrarily or replace them with a generic e-commerce template.

Extend the design consistently to other screens and responsive layouts.

## 5. Demonstrate actual UX expertise

The final result must communicate thoughtful product design, not merely visual decoration.

Ensure that:

- Product information is easy to scan.
- Plant sizes and care requirements are understandable.
- Optional pots and their prices are clear.
- Product images, variants, and pricing remain consistent across the journey.
- Product discovery and category navigation are intuitive.
- Bundle savings and checkout totals are transparent.
- Buttons communicate their purpose.
- Loading, empty, validation, error, unavailable, success, and recovery states receive appropriate design treatment.
- Mobile, tablet, and desktop layouts feel intentionally designed.

Do not remove working functionality or change business logic simply to achieve a visual effect.

## 6. Implementation workflow

Work in the following order:

**Phase A — Audit:** Inspect the repository, references, existing components, tokens, and image assets. Report the principal problems and proposed corrections.

**Phase B — Design direction:** Establish and implement the core visual tokens, typography, surfaces, and image treatment. Show how the proposed direction corresponds to the original references.

**Phase C — Representative screens:** Refine the home page and product detail page first, then apply the same system to the cart and onboarding.

**Phase D — System-wide consistency:** Update shared components and extend the design across the remaining routes without breaking interactions.

**Phase E — Verification:** Run the application and available tests. Check responsive layouts, broken images, accessibility, console errors, and critical shopping journeys.

Inspect existing architecture before selecting a solution. Reuse appropriate components and dependencies rather than rebuilding the entire application unnecessarily.

## 7. Definition of done

The work is not complete merely because the application runs.

The revised application must demonstrate:

- Clear alignment with the original Figma visual direction.
- A distinctive, cohesive premium botanical identity.
- Authentic-looking, appropriately sourced product imagery.
- Intentional and harmonious colour relationships.
- Strong typographic hierarchy and visual composition.
- Consistent components across all important screens.
- Functional, accessible shopping interactions.
- No unsupported claims about image authenticity, testing, or integrations.

After implementation, provide a concise before-and-after audit, identify the files changed, and list any remaining image assets or design decisions that need approval.

Begin with the audit and the highest-impact corrections. Do not make arbitrary cosmetic changes without explaining the design problem they solve.
