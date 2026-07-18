# Phase 10 — Revision Sheet (Active Recall)

> Do NOT open the notes. Answer aloud/on paper, then check and mark ✅/❌. Re-test ❌ items tomorrow.
> Review: after phase → +1 day → +3 days → +1 week → +1 month.

## A. Rapid-fire recall

1. The 4 jobs of a load balancer?
2. L4 vs L7: what does each SEE and decide on? The mailroom/receptionist analogy?
3. ALB vs NLB — 4 differences (routing, speed, static IP, protocols). When must you pick NLB?
4. NGINX algorithms: round_robin vs least_conn vs ip_hash — trade-off of each; why is ip_hash a poor session strategy?
5. What do `max_fails`/`fail_timeout` do? Passive vs active health checks — which does open-source NGINX have?
6. What does `proxy_next_upstream` add for the user experience?
7. ALB anatomy: listener → rule → target group — what does each level decide?
8. What is connection draining (deregistration delay) and which deploy problem does it kill?
9. Design the ideal /health endpoint: what it checks, what it deliberately ignores — and the "checked too much" total-outage story.
10. Rolling deploy with an LB — the step sequence for zero downtime.
11. Blue-green vs canary — mechanics, rollback story, and how the LB/DNS enables each.
12. LB vs API gateway in one line. Name 4 things a gateway adds.
13. How do you get the client's real IP behind an LB, and what silently breaks without it?
14. Timeout chain rule (LB vs app timeouts) — which mismatch causes mystery 502s?
15. The LB itself as SPOF — how is it solved self-hosted vs managed ALB?

## B. Write / draw from memory

- An NGINX `upstream` block with least_conn, 3 servers, max_fails, backup, keepalive.
- The AWS standard stack: Route53 → CloudFront → ALB → TG → instances — with health checks marked.
- The canary weights setup (95/5) in NGINX.

## C. Scenario drill

- Intermittent 502s appeared right after introducing the LB — list 3 plausible causes.
- One backend hangs (not crashes) — which config lines protect users?
- You must deploy at noon peak with zero drops — narrate your exact steps.

## D. Self-score

- 12+ of A → move on. 8–11 → redo lab + re-test tomorrow. <8 → re-read notes actively, redo lab.
