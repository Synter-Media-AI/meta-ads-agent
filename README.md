# Meta Ads MCP Starter Kit — Manage Facebook & Instagram Ads with AI

[![MCP Compatible](https://img.shields.io/badge/MCP-compatible-blue)](https://modelcontextprotocol.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform: Meta Ads](https://img.shields.io/badge/Platform-Meta%20Ads-1877F2)](https://business.facebook.com)

**Run Facebook and Instagram ad campaigns from your code editor.** Open this repo in Amp, Cursor, or VS Code and let your AI agent handle audience building, creative testing, and campaign optimization — no more clicking through Ads Manager.

---

## Why Meta Ads + AI?

Meta's advertising platform reaches 3.3 billion monthly active users across Facebook, Instagram, Messenger, and the Audience Network. It's the most powerful platform for visual products, direct-to-consumer brands, and anyone who needs to reach people based on interests, behaviors, and demographics rather than search intent.

But Meta Ads Manager is notoriously complex. Between campaign objectives, audience overlap, attribution windows, creative fatigue, and the ever-changing algorithm, even experienced media buyers spend hours on routine tasks.

An AI agent cuts through the complexity. It understands Meta's API, knows which campaign objectives map to your goals, and can build Custom Audiences, launch Advantage+ campaigns, and analyze creative performance — all from a chat window.

**Best for:** D2C ecommerce, visual products (fashion, food, home goods), app installs, brand awareness, lead generation for B2C businesses.

---

## Quick Start (30 Seconds)

### Amp / Cursor / VS Code (Copilot)

1. **Get a free API key** at [syntermedia.ai/developer](https://syntermedia.ai/developer)
2. **Set the key:**
   ```bash
   export SYNTER_API_KEY=syn_your_key_here
   ```
3. **Open this repo** in your editor
4. **Start chatting** — MCP tools are pre-configured in `.mcp.json`

### Claude Desktop

Copy `claude_desktop_config.json` to your Claude config directory and replace the API key:

- **macOS:** `~/Library/Application Support/Claude/claude_desktop_config.json`
- **Windows:** `%APPDATA%\Claude\claude_desktop_config.json`

---

## What You Can Do

| Capability | Example |
|-----------|---------|
| **Launch Advantage+ Campaigns** | "Create an Advantage+ Shopping campaign for my Shopify store with $100/day" |
| **Build Custom Audiences** | "Create a Custom Audience from customers who purchased in the last 90 days" |
| **Create Lookalike Audiences** | "Build a 1% Lookalike based on my top 25% customers by revenue" |
| **Upload Ad Creatives** | "Upload this product image and create a carousel ad with 5 slides" |
| **A/B Test Creative** | "Set up an A/B test: lifestyle image vs product-on-white for the spring collection" |
| **Manage Pixel Events** | "Check if my Meta Pixel is firing Purchase events correctly" |
| **Adjust Budgets** | "Double the budget on ad sets with ROAS above 3x" |
| **Audience Exclusions** | "Exclude existing customers from all acquisition campaigns" |
| **Campaign Reports** | "Show me creative performance — which images have the best CTR this month?" |
| **Placement Control** | "How are Instagram Stories performing vs Facebook Feed?" |

---

## Example Conversations

### 1. Launching an Advantage+ Shopping Campaign

> **You:** I run a D2C skincare brand on Shopify. I want to test Meta Ads with $50/day. What's the best approach?
>
> **Agent:** For a D2C ecommerce brand, I'd recommend starting with **Advantage+ Shopping Campaign (ASC)**. Meta's algorithm is exceptionally good at finding buyers when it has product catalog data.
>
> Here's what I'll set up:
> - **Objective:** Sales (OUTCOME_SALES)
> - **Budget:** $50/day
> - **Audience:** Broad targeting (let Advantage+ find the right people)
> - **Placements:** Advantage+ (all placements — the algorithm will optimize)
> - **Creative:** 5 product images with dynamic headlines
> - **Pixel:** Purchase event for optimization
> - **Existing customer cap:** 20% (so 80% of budget goes to new customers)
>
> The key: Advantage+ works best with minimal targeting restrictions. Resist the urge to narrow the audience — Meta's ML is better at finding buyers than manual targeting.
>
> **You:** Go for it. But set the existing customer cap to 10%.
>
> **Agent:** Done. ASC campaign created with 10% existing customer budget cap. I've also excluded your email list of 12,400 customers from acquisition so you're not paying to reach people who already buy from you. Campaign is PAUSED — say "enable" when ready.

### 2. Diagnosing Creative Fatigue

> **You:** My CPAs have been creeping up for 3 weeks. Is my creative getting stale?
>
> **Agent:** Let me pull creative-level metrics for the last 30 days...
>
> **Diagnosis: Creative fatigue confirmed.** Here's the evidence:
>
> | Creative | Week 1 CPA | Week 4 CPA | Frequency | CTR Trend |
> |---|---|---|---|---|
> | "Glow Serum — Hero" | $18.20 | $31.40 | 4.7 | 2.1% → 0.9% |
> | "Before/After" | $15.80 | $22.10 | 3.9 | 3.4% → 1.8% |
> | "Testimonial Video" | $21.50 | $24.30 | 2.1 | 1.8% → 1.5% |
>
> Your top creative ("Glow Serum — Hero") has a frequency of 4.7 — meaning the average person has seen it almost 5 times. CTR has dropped by 57%.
>
> **Recommended action:**
> 1. Pause "Glow Serum — Hero" (it's burned out)
> 2. Introduce 3-5 new creatives immediately
> 3. The "Testimonial Video" still has runway (frequency only 2.1) — keep it running
> 4. Want me to generate new ad images using AI?

### 3. Building a Lookalike Audience Strategy

> **You:** I have 5,000 customers in my email list. How should I use them for targeting?
>
> **Agent:** Your 5,000-customer email list is a goldmine. Here's a layered Lookalike strategy:
>
> **Step 1: Upload & segment your list**
> - Top 25% by lifetime value → "High-Value Customers" Custom Audience
> - All purchasers → "All Customers" Custom Audience
> - Repeat purchasers (2+ orders) → "Repeat Buyers" Custom Audience
>
> **Step 2: Create Lookalikes**
> - 1% Lookalike of High-Value Customers (highest quality, ~2.3M people in US)
> - 1% Lookalike of Repeat Buyers (loyalty signals)
> - 3% Lookalike of All Customers (broader reach for scaling)
>
> **Step 3: Campaign structure**
> - Cold prospecting: Target 1% High-Value Lookalike, exclude all customers
> - Scale: Target 3% All Customers Lookalike, exclude 1% Lookalikes (avoid overlap)
> - Retention: Target "All Customers" with new product launches
>
> Want me to create these audiences now? I'll need your customer CSV or I can pull from your connected Shopify/Klaviyo.

### 4. Instagram-Specific Strategy

> **You:** I'm a fashion brand. Should I focus on Instagram only?
>
> **Agent:** Tempting, but no — and here's why. Let me pull your placement breakdown...
>
> | Placement | Spend | CPA | ROAS |
> |---|---|---|---|
> | Instagram Feed | $1,200 | $24.30 | 3.8x |
> | Instagram Stories | $890 | $19.10 | 4.5x |
> | Instagram Reels | $440 | $17.80 | 5.1x |
> | Facebook Feed | $780 | $21.50 | 4.1x |
> | Facebook Marketplace | $190 | $16.20 | 5.8x |
>
> **Surprise: Facebook Marketplace has your best ROAS (5.8x) and lowest CPA ($16.20).** Fashion brands often ignore Marketplace, but shoppers there have high purchase intent.
>
> Instagram Reels is also outperforming Stories and Feed — worth allocating more creative effort to short-form video.
>
> **My recommendation:** Keep Advantage+ placements ON, but create separate ad sets with Reels-first and Marketplace-optimized creative.

### 5. Pixel Troubleshooting

> **You:** I launched a campaign yesterday with Purchase optimization but I'm getting 0 conversions even though Shopify shows 12 orders.
>
> **Agent:** Let me diagnose your Meta Pixel setup...
>
> **Found the issue:** Your Pixel is firing `Purchase` events, but the `content_ids` parameter doesn't match your product catalog IDs. The Pixel sends SKU format (`SKN-001`) but your catalog uses Shopify product IDs (`7891234567890`).
>
> This means Meta can't attribute purchases back to the ads. The fix:
>
> 1. Update your Pixel to send Shopify product IDs (not SKUs) in `content_ids`
> 2. Or update your product catalog to use SKUs as the `id` field
>
> Additionally, I see your `PageView` event fires on every page but `ViewContent` only fires on 3 of your 47 product pages — your Pixel installation is incomplete.
>
> Want me to help fix the Pixel configuration?

---

## Meta Ads Tips from the Pros

1. **Start with Advantage+ Shopping for ecommerce.** It consistently outperforms manually-targeted campaigns for product sales. Give it broad targeting and 3-5 diverse creatives.
2. **Minimum budget: $5/day per ad set.** But $20-30/day is more practical — Meta needs ~50 conversions per week per ad set to optimize. At a $30 CPA, that's $215/week ($30/day).
3. **Creative is your targeting.** Meta's algorithm is so good at finding buyers that your creative does more targeting work than your audience settings. A video showing rock climbing will reach climbers, regardless of interest targeting.
4. **Refresh creative every 2-3 weeks.** Creative fatigue is the #1 performance killer on Meta. Track frequency — when it passes 3.0, performance drops.
5. **Use the Conversions API alongside Pixel.** With iOS 14.5+ privacy changes, client-side Pixel misses ~30% of conversions. Server-side Conversions API fills the gap.
6. **Lookalike audiences decay.** Refresh your source audiences monthly. Customer lists from 6 months ago no longer represent your current best buyers.
7. **Don't over-segment ad sets.** Meta's algorithm works best with larger audiences. Instead of 10 ad sets with narrow targeting, use 2-3 ad sets with broad targeting and diverse creative.

---

## FAQ

### Can Claude manage my Facebook Ads?
Yes. This MCP starter kit gives Claude (or any MCP-compatible agent) full access to the Meta Ads API — create campaigns, manage audiences, upload creatives, adjust budgets, and pull reports.

### Does this work with Instagram Ads?
Yes. Instagram and Facebook ads are managed through the same Meta Ads platform. You can target Instagram-only placements or let Meta optimize across both.

### Is there an MCP for Meta Ads?
You're looking at it. This repo pre-configures the Synter MCP server for Meta Ads management. Works with Amp, Cursor, VS Code, and Claude Desktop.

### Can the agent create Lookalike Audiences?
Yes. Upload a customer list or use website visitors, and the agent can create 1%, 2%, 5%, or 10% Lookalike Audiences. It can also recommend which source audience will produce the best Lookalikes.

### Do I need Facebook Business Manager?
Yes. You need a Meta Business Manager account with an ad account. If you don't have one, [create it here](https://business.facebook.com). Connect it via OAuth at [syntermedia.ai/settings](https://syntermedia.ai/settings/credentials).

### How does this handle iOS privacy changes?
The agent can set up server-side Conversions API (CAPI) alongside your Meta Pixel, which recovers attribution data lost to iOS 14.5+ App Tracking Transparency.

---

## Related Repos

- [google-ads-agent](https://github.com/Synter-Media-AI/google-ads-agent) — Google Search & PMax campaigns
- [tiktok-ads-agent](https://github.com/Synter-Media-AI/tiktok-ads-agent) — Short-form video ads
- [audience-sync-agent](https://github.com/Synter-Media-AI/audience-sync-agent) — Sync audiences across platforms
- [ai-creative-agent](https://github.com/Synter-Media-AI/ai-creative-agent) — Generate ad images & videos
- [shopify-agent](https://github.com/Synter-Media-AI/shopify-agent) — Sync Shopify products & customers
- [cross-platform-ads-agent](https://github.com/Synter-Media-AI/cross-platform-ads-agent) — Manage all platforms together

---

## License

MIT — see [LICENSE](LICENSE) for details.

Built by [Synter](https://syntermedia.ai) · [Get API Key](https://syntermedia.ai/developer) · [Documentation](https://syntermedia.ai/docs)
