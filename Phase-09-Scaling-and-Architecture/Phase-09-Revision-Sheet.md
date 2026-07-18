# Phase 09 — Revision Sheet (Active Recall)

> Do NOT open the notes. Answer aloud/on paper, then check and mark ✅/❌. Re-test ❌ items tomorrow.
> Review: after phase → +1 day → +3 days → +1 week → +1 month.

## A. Rapid-fire recall

1. What actually happens when load exceeds one server's capacity (the failure chain to 504)?
2. Vertical vs horizontal scaling — pros/cons of each; when is vertical the RIGHT answer?
3. What does horizontal scaling REQUIRE of the app? The interview one-liner about statelessness?
4. The stateful-app bug with 2 instances (login/session story) — tell it.
5. Where does each go when externalized: sessions? files? cache? scheduled jobs? (4 answers)
6. Sticky sessions — what are they and 2 reasons they're the crutch, not the fix?
7. Cache-aside pattern — recite the read path. Which Spring annotations?
8. The two hard cache problems: invalidation and stampede — one defense each.
9. What data is safe to cache; what isn't? (the 3 criteria)
10. The database scaling playbook IN ORDER (6 steps) — why is order the whole point?
11. Read replicas: how does replication work, what is lag, and what reads must NOT go to a replica?
12. Read-your-own-writes: the user story + 2 fixes.
13. Connection-pool math: 10 instances × pool 50 vs max_connections 100 — what happens?
14. Availability nines: 99.9% = how much downtime/year? What does each extra nine cost?
15. Define SPOF. How do you hunt SPOFs? (walk which path?)
16. Multi-AZ vs read replica — HA or scaling? (the classic!)
17. Recite the standard scaling story (1 server → … → sharding) and what triggers each arrow.

## B. Write from memory

- The horizontal-scaling diagram (LB, 3 stateless apps, shared Redis + DB) — mark where sessions and files live.
- The caching-layers chain from browser to DB (5 layers).

## C. Scenario drill (answer in 2–3 sentences each)

- p95 doubled at 2× traffic — first 3 metrics you look at?
- Users randomly logged out after adding a second app server — cause and fix?
- Product page shows old price for 10 minutes after update — which mechanism, which fixes?

## D. Self-score

- 14+ of A → move on. 9–13 → redo lab + re-test tomorrow. <9 → re-read notes actively, redo lab.
