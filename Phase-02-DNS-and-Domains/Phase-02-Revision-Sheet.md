# Phase 02 — Revision Sheet (Active Recall)

> Do NOT open the notes. Answer aloud/on paper, then check and mark ✅/❌. Re-test ❌ items tomorrow.
> Review: after phase → +1 day → +3 days → +1 week → +1 month.

## A. Rapid-fire recall

1. What problem does DNS solve? Why not just use IPs? (2 reasons)
2. Break `https://api.shop.example.com` into its parts: TLD, registered domain, subdomains.
3. What does a registrar actually record when you buy a domain?
4. Name the 4 server types in resolution: recursive resolver, root, TLD, authoritative — one line each.
5. Recite the full resolution walk for a cold cache (7 steps, including the 3 cache checks first).
6. What is TTL? What does TTL 300 vs 86400 mean in practice?
7. Where can a DNS answer be cached? (list all layers)
8. A record vs AAAA vs CNAME vs MX vs TXT vs NS — one line each.
9. Why can't you put a CNAME on the root domain?
10. "I changed DNS but the old site still loads" — explain, and how to verify the change is live.
11. The migration TTL trick: what do you do days before switching servers, and why?
12. DNS resolves fine but the site doesn't load — DNS problem or server problem? How do you prove it?
13. Does DNS use TCP or UDP? Port?
14. Which two dig commands show (a) just the IP, (b) the real root→TLD→auth walk?

## B. Draw / write from memory

- The DNS hierarchy tree (root → TLD → authoritative) with what each level answers.
- The record table for: site+api on VPS `203.0.113.50`, blog on external `myblog.hashnode.dev`, Google mail. (type, name, value, TTL)

## C. Command drill — what does each do?

```
dig example.com +short        dig example.com +trace       dig example.com MX
dig @1.1.1.1 example.com      dig example.com NS +short    nslookup example.com
```

## D. Self-score

- 11+ of A → move on. 7–10 → redo lab + re-test tomorrow. <7 → re-read notes actively, redo lab.
