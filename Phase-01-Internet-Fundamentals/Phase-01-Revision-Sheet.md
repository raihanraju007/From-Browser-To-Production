# Phase 01 — Revision Sheet (Active Recall)

> Do NOT open the notes. Answer aloud/on paper, then check and mark ✅/❌. Re-test ❌ items tomorrow.
> Review: after phase → +1 day → +3 days → +1 week → +1 month.

## A. Rapid-fire recall

1. Define the Internet in two ideas (physical + rules). Why "network of networks"?
2. Client vs server — roles or machines? Who always initiates?
3. Give an example of one program being client AND server at once.
4. What is a packet? Name the 3 things every packet carries besides data.
5. Why packets instead of sending data whole? (3 reasons)
6. IPv4 vs IPv6 — bits, format, why IPv6 exists?
7. Recite the 3 private IP ranges. Which does AWS use? Docker? Home routers?
8. What is 127.0.0.1? Why can't a teammate open your localhost?
9. Binding to `127.0.0.1` vs `0.0.0.0` — difference and when it bites you?
10. IP vs MAC — which analogy? Which layer uses each?
11. Switch vs router — what does each connect, by which address?
12. Explain NAT in 3 sentences. Why can't the Internet initiate a connection to your laptop?
13. What is a port? Recite the ports: SSH, HTTP, HTTPS, DNS, PostgreSQL, Redis, MySQL, Spring Boot default.
14. What error do you get when two programs want the same port? Which commands diagnose it?
15. Recite the TCP 3-way handshake (the 3 message names).
16. What 3 guarantees does TCP give? What does UDP drop, and what does it gain?
17. Name a use case where UDP is the RIGHT choice and why.
18. Recite the 7 OSI layers bottom-up, one protocol/device each.
19. What lives at L3, L4, L7? What is a "L7 load balancer"?
20. Recite the debugging ladder with a command per step (L1→L7).

## B. Draw from memory

- The full request journey: browser → WiFi → router (NAT) → ISP → routers → server, labeled with private IP, public IP, port, TCP, L-numbers.
- The NAT translation table example (who rewrote what).

## C. Command drill — what does each show/do?

```
ip addr          curl ifconfig.me      ip route
ping -c4 host    traceroute host       ss -tulpn
lsof -i :8080    nc -zv host 443       curl -v https://example.com
```

## D. Self-score

- 16+ of A → move on. 10–15 → redo lab + re-test tomorrow. <10 → re-read notes actively, redo lab.
