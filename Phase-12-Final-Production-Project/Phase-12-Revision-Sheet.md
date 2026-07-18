# Phase 12 — Capstone Readiness Sheet (Final Self-Exam)

> This is the whole-course exam. Everything from memory, out loud or on paper. If any item fails, the phase number to revisit is marked.

## A. The grand narration (the interview king)

Narrate `https://shop.example.com/api/orders` from pressing Enter to rendered response, naming EVERY hop, protocol, and port:

```
browser → DNS resolution (which 4 servers?) → TCP handshake → TLS handshake
→ CloudFront edge (hit or miss?) → ALB (listener→rule→target group→health)
→ NGINX (which headers added?) → Spring Boot → Redis (session? cache?)
→ RDS → response back through every layer
```
Score yourself hop by hop. Gaps: P1 (TCP/IP), P2 (DNS), P3 (TLS), P5 (NGINX), P8 (CDN), P10 (ALB).

## B. "Why does it exist?" — one paragraph each, no notes

1. Why NGINX when there's already an ALB? (P5/P10)
2. Why must the app be stateless, and where did every kind of state go? (P9)
3. Why is RDS in a private subnet — trace the exact blocking mechanism? (P8)
4. Why Redis — both of its jobs here? (P9)
5. Where does TLS terminate, and why there? (P3/P5/P10)
6. Why containers, when a jar + systemd works? (P4/P6)
7. What are your RPO and RTO, and which choices set them? (P7)

## C. Failure drill — what happens, who notices, what do you do?

| Failure | What absorbs it? | Your first command |
|---|---|---|
| One app container dies | ? | ? |
| A whole EC2 instance dies | ? | ? |
| RDS primary fails (Multi-AZ) | ? | ? |
| Bad build fails readiness | ? | ? |
| An AZ goes dark | ? | ? |
| Disk fills on one instance | ? | ? |

## D. Operations from memory

- The zero-downtime deploy sequence, step by step, including draining and rollback command.
- The restore-from-backup drill, timed steps.
- The "site is down" decision tree: DNS → CDN → LB → NGINX → app → DB, one command per hop.

## E. Ready to build?

All of A–D solid → start Milestone M1 in the Phase-12 notes. Any section shaky → that's your revision target this week; the capstone will mercilessly expose it anyway. 🚀
