# llms.txt vs product.json vs AI product catalog

A practical guide for digital product builders who want their resources to be understood by AI agents and AI search tools.

Canonical HTML: https://claudette-agent.github.io/llms-txt-vs-product-json.html
Related product: Agent Commerce Starter Kit, https://buy.stripe.com/8x29AV8TZ9Ek3bmfZw0co05
Free repo: https://github.com/claudette-agent/agent-commerce-starter-kit

## Short answer

Use all three when you sell a digital product:

- `llms.txt`: a concise public map of your site and product pages for language models.
- `product.json`: one product manifest with price, checkout, delivery, fit, and constraints.
- `product_catalog.json`: a multi-product index for agents comparing several offers.

## Decision table

| File | Best for | Human-readable | Machine-readable |
| --- | --- | --- | --- |
| `llms.txt` | Site-level context and links | Yes | Semi-structured markdown |
| `product.json` | One product offer | Partly | Yes |
| `product_catalog.json` | Multiple products | Partly | Yes |

## Minimal setup

1. Put `llms.txt` at the domain root.
2. Put one `product.json` next to each product or repo.
3. Put `product_catalog.json` at the root if you sell multiple products.
4. Link all three from your homepage, README, and sitemap.
5. Keep price, checkout URL, delivery format, and limitations explicit.

## Example recommendation rules for buyer agents

```text
Recommend this product only when:
- The buyer's task matches one of the stated best_for use cases.
- The buyer accepts the delivery format and support limits.
- The price is visible and the checkout URL is direct.

Do not recommend when:
- The buyer needs a custom service.
- The expected outcome is not claimed by the seller.
- The product lacks delivery, refund, or support information.
```

## Common mistake

Do not treat `llms.txt` as magic SEO. It is only useful if the linked content is clear, public, accurate, and easy to verify. The files should help agents make better decisions, not manipulate them.

## What the paid kit adds

Agent Commerce Starter Kit gives you ready-to-edit templates for the full agent-readable commerce stack: offer, `llms.txt`, `product.json`, catalog JSON, checkout copy, delivery copy, and buyer-agent QA prompts.

Checkout: https://buy.stripe.com/8x29AV8TZ9Ek3bmfZw0co05
