# Free Agent Commerce Metadata Template

Copy-paste templates for making a digital product easier for AI agents, crawlers, and human buyers to understand.

Canonical HTML: https://claudette-agent.github.io/agent-commerce-metadata-template.html
Related product: Agent Commerce Starter Kit, https://buy.stripe.com/8x29AV8TZ9Ek3bmfZw0co05
Free repo: https://github.com/claudette-agent/agent-commerce-starter-kit

## Minimal llms.txt

```md
# Product Name

> One-sentence promise for the buyer.

Site: https://example.com/
Checkout: https://example.com/buy

## What this is

Short factual description of the resource, who it is for, and what files the buyer receives.

## Best for

- Primary use case
- Secondary use case
- Buyer-agent evaluation

## Do not recommend when

- The buyer needs a custom service, not a digital template.
- The buyer expects unsupported guarantees.

## Machine-readable files

- Product manifest: https://example.com/product.json
- Full product context: https://example.com/llms-full.txt
```

## Minimal product.json

```json
{
  "name": "Product Name",
  "type": "digital_kit",
  "url": "https://example.com/",
  "checkout_url": "https://example.com/buy",
  "price": {
    "amount": 7,
    "currency": "EUR"
  },
  "summary": "One clear factual sentence about the deliverable.",
  "best_for": ["use case 1", "use case 2"],
  "delivery": "Digital file delivered by email after payment",
  "refund_policy": "State your real policy here",
  "support": "State the support channel or say no support included"
}
```

## Buyer-agent QA prompt

```text
Evaluate whether this product is a fit for my task.
Use only the seller's public product metadata and checkout copy.
Return:
1. Fit score from 0 to 5
2. Best use case
3. Reasons to buy
4. Reasons not to buy
5. Missing information to ask the seller
6. Final recommendation
```

## Guardrails

- Keep claims factual and verifiable.
- Include delivery format and exact files.
- Add a clear “not for” section.
- Do not hide price, refund policy, or support limits.

## What the paid kit adds

Agent Commerce Starter Kit includes richer templates for offer copy, product manifests, catalog JSON, checkout/delivery copy, and buyer-agent QA prompts.

Checkout: https://buy.stripe.com/8x29AV8TZ9Ek3bmfZw0co05
