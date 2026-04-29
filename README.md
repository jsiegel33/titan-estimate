# Titan Cost Estimate Tool

A single-file HTML app that gives a preneed insurance agent a ranged ballpark funeral cost estimate in under 60 seconds. Show this to the family *before* opening Prelude to write the actual policy.

## How to Run

Open `titan-estimate.html` in any browser. No server, no build step, works offline.

## How to Edit Pricing

The `PRICING` object starts at **line ~139** inside the `<script>` tag. Each category has `lo`, `mid`, `hi` values in dollars.

### Adding or Changing a State Tax Rate

Find the `stateTaxRate` object inside `PRICING` (around line 148). Add or update a two-letter state code:

```js
stateTaxRate: { FL: 0.06, CA: 0.0725, /* ... */ }
```

All rates are placeholders — cross-check with Prelude's live tax logic before using with families.

## v2 Roadmap

- PDF export (beyond browser print)
- Global Atlantic API integration for live premium quotes
- Saved estimates / history
- Analytics and usage tracking
- Multi-agent support (per-agent branding/contact info)
- Actual health-question flow affecting premium range
