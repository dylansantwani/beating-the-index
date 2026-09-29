# Beating the Index

Item-number enumeration, anonymous market comps, and the economics of sub-minute RAM arbitrage on eBay

Dylan Santwani · September 2026 · [PDF](beating-the-index.pdf)

## Abstract

Resale arbitrage on eBay depends on two things: seeing an underpriced listing before other buyers, and knowing what it will really sell for. For used computer memory both are harder than they look. eBay's search index shows a new listing a median of 256 seconds after it goes live, and never sooner than 137 seconds in our data. Sold-price data is locked behind a Seller Hub research tool whose sessions expire unpredictably. We describe a two-part system built and run over two weeks. RAM Live finds new listings by walking eBay's item-number counters directly. ram_platform values each one against exact-part-number sold comparables from Terapeak. Over 24,549 RAM listings detected in 5.5 days, RAM Live read listings a median of 5.1 s after they started. That is within about two seconds of the earliest moment eBay serves them, and roughly 50 times faster than search. It saw a listing before search in 7,785 of 7,886 cases (98.7%). Two-thirds of the RAM it found never appeared in any of our search feeds at all.

The harder finding is economic. Once listings are priced honestly (same part number, same kit layout, used condition, capped shipping), the market is close to efficient. Only 1.9% of estimated listings and 1.7% of exact-comp listings show a positive net after fees. A listing's estimated ROI strongly predicts whether it sells within a day, rising from 1% at deeply negative ROI to about 60–66% at ROI of zero or better. The system flagged 46 deals in the window. 27 of them sold to someone within 24 hours, at a median of 22 minutes after listing. So detection is solved. The binding constraints are now valuation recall, the alert path (median about 58 s to a phone), and the capital and willingness to buy quickly. We also document an adversarial timeline: four distinct eBay edge blocks in 48 hours, each aimed at whichever single request signature carried our traffic. And we record a set of engineering failure modes that account for most of the lost time.

## Cite

```bibtex
@misc{santwani2026beating,
  author = {Santwani, Dylan},
  title  = {Beating the Index: Item-Number Enumeration, Anonymous Market Comps, and the Economics of Sub-Minute RAM Arbitrage on eBay},
  year   = {2026},
  month  = sep,
  url    = {https://github.com/dylansantwani/beating-the-index}
}
```
