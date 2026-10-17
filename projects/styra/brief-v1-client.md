# Styra — V1 Client Brief

**Document:** `projects/styra/brief-v1-client.md`  
**Product:** Styra  
**Version:** V1 — Initial Product Design  
**Status:** Draft for review

## 1. Client and Product Background

Styra is an AI-powered shopping assistant designed to help customers find suitable products across multiple online stores and relevant marketplaces.

Instead of requiring customers to search manually, browse numerous websites, and compare products themselves, Styra helps them explain what they need through a natural text-based conversation. It then researches available options, compares relevant information, and presents a focused shortlist to support their purchasing decision.

Customers may be looking for branded, non-branded, or second-hand products, depending on their needs, budget, and preferences.

Styra's primary purpose is to make online shopping more efficient, relevant, and less frustrating while helping customers make informed purchasing decisions.

## 2. Problem Statement

Online shopping can require considerable time and effort. Customers often visit multiple websites, compare prices, read reviews, evaluate product quality, and try to determine which option best meets their needs.

The problem becomes more difficult when customers:

- Have a limited budget but still want good quality.
- Do not know which brands or products offer the best value.
- Are unsure how to describe exactly what they need.
- Need to compare branded, non-branded, and second-hand alternatives.
- Feel overwhelmed by too many choices or irrelevant recommendations.
- Spend too much time searching without feeling confident about their final decision.

Traditional search tools generally require customers to know what to search for and how to filter the results.

Styra aims to reduce this burden by understanding the customer's needs, performing relevant product research, and presenting useful comparisons with minimal unnecessary interaction.

## 3. Target Users

Styra's initial target users include people who:

- Want to save time and effort when shopping online.
- Need to find suitable products within a specific budget.
- Want to balance price, quality, style, and practical requirements.
- Find it difficult to compare products across multiple retailers.
- Know exactly what they want, as well as customers who need guidance to clarify their requirements.

These are initial target-user hypotheses and should be validated through user research.

## 4. Core Product Goals

### Goal 1: Save customers time and effort

Reduce the need to browse multiple websites, perform repetitive searches, and compare large numbers of products manually.

### Goal 2: Deliver relevant recommendations

Recommend products that match the customer's stated needs, budget, preferences, and intended use—not merely products that contain matching keywords.

### Goal 3: Help customers find good value

Help customers understand the trade-offs between price and available quality evidence. A cheaper product should not automatically be considered better value, and a branded product should not automatically be considered higher quality.

### Goal 4: Make shopping feel effortless

Keep the interaction simple and conversational. Customers should not feel that they must complete a questionnaire before receiving help.

### Goal 5: Support confident decisions

Explain why products are recommended, show meaningful differences, disclose important limitations, and leave the final purchasing decision to the customer.

## 5. Core Features — V1

### 5.1 Conversational AI Shopping Assistant

Customers can describe what they want using natural language.

For example:
- "I need a dress."
- "Find me an elegant dress for an office party under €50."
- "I need comfortable formal trousers for work."

Customers may provide detailed requirements immediately or start with only a product name.

Styra should interpret the information provided and guide the customer only when additional clarification would meaningfully improve the search.

### 5.2 Guided Shopping Prompts

Some customers may not know which details will help Styra find suitable products.

The interface should provide optional examples that help customers describe their requirements more effectively.

Suggested prompt categories include:

- **Product:** Dress, T-shirt, skirt, formal trousers or suit.
- **Occasion or usage:** Office party, work, everyday wear or a special event.
- **Budget:** Under €50 or another preferred spending limit.
- **Style and colour:** Elegant, professional, casual, black or another preferred colour.
- **Size and fit:** Relevant sizing and fit preferences.
- **Material or season:** Cotton, linen, silk, lightweight fabric or summer clothing.

These examples should guide customers without requiring them to provide every detail.

Customers should be able to start with a simple request, add optional details, or continue naturally through conversation.

### 5.3 Adaptive Questioning

Styra should ask questions selectively rather than following a fixed questionnaire.

The interaction should follow these principles:

- Understand the information the customer has already provided.
- Identify missing details that could materially affect product suitability.
- Ask a concise follow-up question only when it is useful.
- Avoid asking for information that is already known or unnecessary.
- Begin searching as soon as sufficient information is available for a meaningful search.

For example, if a customer provides the product type, budget, size, colour, and intended occasion, Styra should not delay the search by asking for those details again.

The objective is to improve search quality without increasing customer effort unnecessarily.

### 5.4 Relevant Multi-Store Product Research

Styra should research available products across multiple online stores and relevant marketplaces, subject to available data sources and technical capabilities.

The research should consider the customer's requirements rather than relying only on basic keyword matching.

Relevant comparison factors may include:

- Price and fit within the customer's budget.
- Product specifications, materials, and available size information.
- Customer reviews and ratings, where available.
- Available evidence of quality and durability.
- Product condition, particularly for second-hand items.
- Shipping costs and delivery information, where available.
- Other factors that directly affect the customer's needs.

Styra should not assume that all information is available or verified. It must communicate important uncertainties honestly.

### 5.5 Curated Product Recommendations

Styra should aim to present approximately three to four highly relevant product options when sufficient suitable options are available.

The objective is not to fill a fixed number of slots. It is to help customers identify suitable choices quickly.

Each recommendation should communicate:

- Product name and image.
- Price and retailer.
- Relevant product details.
- Why the product matches the customer's requirements.
- Important advantages and limitations.
- Available quality evidence and relevant review information.
- Any significant uncertainty about price, stock, condition, or product details.

Recommendations should provide meaningful alternatives rather than several nearly identical products without a clear reason.

### 5.6 Product Comparison

Customers should be able to compare shortlisted products using the information most relevant to their decision.

The comparison should make differences easy to understand, including price, product features, materials, available quality evidence, reviews, condition, and suitability for the intended use.

The goal is to help customers understand trade-offs rather than simply rank products by price.

### 5.7 Search Refinement When No Suitable Match Is Found

Styra should not present irrelevant products merely to complete a shortlist.

If it cannot find suitable options, it should:

1. Explain the situation politely and clearly.
2. Avoid implying that unavailable or unverified products have been found.
3. Identify a relevant alternative where possible, such as relaxing a non-essential preference or considering suitable second-hand options.
4. Ask for the customer's consent before changing important requirements.
5. Refine the search using the customer's response.

The customer should remain in control of their budget and preferences.

### 5.8 Optional Traditional Search

Although conversational AI is the primary experience, customers should also be able to use conventional product search and filters when preferred.

This provides flexibility for customers who already know what they want or prefer a more direct search experience.

## 6. Core Customer Journey

The intended V1 experience follows this sequence:

**Customer describes needs → Styra understands and clarifies when necessary → Styra researches available products → Styra presents a relevant shortlist → Customer compares options → Customer decides.**

The experience should remain flexible. Customers who provide sufficient information immediately should be able to move directly to search without unnecessary follow-up questions.

## 7. Design Requirements and Principles

The V1 experience should follow these requirements:

### Customer-centred problem-solving

Every major interaction should help customers find a suitable product, save time, reduce effort, or make a more informed decision.

### Minimal interaction burden

Avoid unnecessary questions, repetitive information requests, excessive steps, and long forms.

### Relevant recommendations over result quantity

Prioritise product suitability and meaningful comparisons over the number of results displayed.

### Clear and transparent communication

Explain recommendations in plain language. Distinguish verified information from unavailable, estimated, or unverified information.

### Customer control

Do not silently change the customer's budget, preferences, or requirements. Ask permission before broadening important constraints.

### Clear visual hierarchy

Help customers understand the next step, compare product information quickly, and identify the most important differences without visual clutter.

### Accessibility and responsive usability

Ensure that essential interactions, text, controls, and product comparisons remain usable across supported screen sizes and accessible interaction methods.

### Honest product representation

Do not make unsupported claims about product quality, authenticity, stock availability, prices, or retailer coverage.

## 8. V1 Scope Boundaries

### Included in the initial design scope

- Conversational shopping through text.
- Optional guided prompts and example requests.
- Context-sensitive follow-up questions.
- A product discovery and research experience.
- Curated product results and comparisons.
- Branded, non-branded, and relevant second-hand options where available.
- Search refinement when suitable matches are unavailable.
- Optional traditional search and filters.
- Loading, empty, error, and unavailable-information states.
- Clear paths for customers to continue to a retailer and make their purchasing decision.

### Not assumed to be solved in V1

The following capabilities require separate feasibility, technical, or business validation:

- Guaranteed real-time prices and stock across every retailer.
- Comprehensive product coverage across all online stores and marketplaces.
- Universal verification of product quality, authenticity, sellers, or second-hand condition.
- Guaranteed discovery of the objectively best product in every search.
- In-app checkout, payments, and order management.
- A confirmed monetisation or affiliate business model.
- A fully validated customer segment or product-market fit.

The initial design should communicate realistic capabilities and limitations rather than imply that these challenges have already been solved.

## 9. Initial Success Criteria

The V1 design should make it possible to evaluate whether customers can:

- Start shopping with either a simple product name or a detailed request.
- Understand which additional details may improve their search without being forced to provide all of them.
- Complete a useful search without unnecessary questioning.
- Find a shortlist that reflects their needs, preferences, and budget.
- Understand why products are recommended and how they differ.
- Identify important product limitations and unverified information.
- Refine their search when suitable products are unavailable.
- Continue to a retailer to review or purchase a chosen product.

Quantitative targets should be established after initial usability testing and baseline measurement.

## 10. Open Questions for Future Validation

The following questions remain open and should not block the initial design unless they materially affect a core interaction:

- Which product categories should be prioritised for launch?
- Which retailers and marketplaces can realistically be covered?
- What data sources or integrations will support product research?
- How frequently can prices, stock, and product information be refreshed?
- What evidence should Styra use to assess quality and value?
- Which launch markets and languages should be supported?
- What privacy and legal requirements apply to customer conversations and product data?
- How will the product be monetised sustainably?

These questions will inform subsequent validation and feasibility work.

## 11. V1 Product Definition

Styra is a conversational AI shopping assistant that helps customers find suitable products within their budget through relevant research, transparent comparison, and minimal unnecessary interaction.

Its central promise is to help customers make better-informed shopping decisions while spending less time searching, browsing, and comparing products manually.

**Core principle: Find the right options with less effort—not simply more options with more interaction.**
