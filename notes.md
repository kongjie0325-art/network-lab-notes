# Day 1

Started learning basic network diagnostics.

- Tested ping latency
- Learned about packet loss
# Day 2 - Traceroute Analysis

## Objective
Analyze network routing path and latency behavior

---

## Test Targets
- google.com
- cloudflare.com
- 8.8.8.8

---

## Traceroute Results

### google.com
- Total hops: 12
- First latency spike: Hop 6
- Notes:
  - Latency increases from 18ms → 32ms at hop 6
  - Route stabilizes after hop 8

### cloudflare.com
- Total hops: 10
- Path difference:
  - Shorter path compared to google
  - Lower latency overall (~15ms avg)

### 8.8.8.8
- Observations:
  - Similar path to google
  - Slightly more stable latency

---

## MTR Results

### google.com
- Avg latency: 24 ms
- Packet loss: 0.0 %
- Best: 12 ms
- Worst: 41 ms
- Stability:
  - Generally stable, minor jitter

---

## Analysis

1. Bottleneck location:
   - Minor latency increase at mid-route (likely ISP backbone)

2. Routing behavior:
   - Cloudflare uses more optimized CDN routing (fewer hops)

3. Network quality:
   - Low latency, no packet loss, stable connection

---

## Conclusion

- Network path complexity: medium
- Stability: good
- Suitable for latency-sensitive applications

---

## Next Step

- Analyze VPS routing
- Compare different server locations
## Notes
This analysis is based on simulated but realistic network behavior.
