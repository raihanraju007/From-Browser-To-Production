# Phase 07 — Revision Sheet (Active Recall)

> Do NOT open the notes. Answer aloud/on paper, then check and mark ✅/❌. Re-test ❌ items tomorrow.
> Review: after phase → +1 day → +3 days → +1 week → +1 month.

## A. Rapid-fire recall

1. What is a VPS? What does it give you that your NAT-ed laptop can't (Phase 1 link)?
2. Shared hosting vs VPS vs dedicated vs cloud — the analogy and when each fits.
3. Recite the first-30-minutes security ritual IN ORDER (8 steps). Which step must you verify before disabling passwords?
4. Why do bots attack a fresh server within minutes? Where do you see the evidence?
5. What does fail2ban add on top of key-only SSH?
6. The two deployment approaches (systemd classic vs compose) — why does the Phase-6 compose file run unchanged?
7. Which DNS records connect the domain, and how do you verify propagation before testing HTTP?
8. Why must DNS point at the server BEFORE certbot can issue a cert? (the challenge mechanism)
9. Why monitor from OUTSIDE the server? Why a /health endpoint instead of just port 443?
10. "A backup you haven't restored is a hope" — what's the full backup recipe (dump, ship off-server, automate, test)?
11. What are RPO and RTO in plain words? What sets your data-loss window?
12. In deploy.sh: what do `set -e` and the final `curl -f /health` each prevent?
13. Name 4 classic VPS mistakes that cause lockouts or breaches.
14. Why does a 1 GB RAM VPS randomly kill your JVM, and the fix?

## B. Write from memory

- The full milestone diagram: browser → DNS → VPS public IP → ufw → NGINX(TLS) → app → DB — every hop labeled with what YOU configured there.
- The disaster-recovery runbook skeleton (server gone; you have git + last dump).

## C. Command drill

```
ssh-copy-id deploy@ip          nano /etc/ssh/sshd_config (which 2 lines?)
ufw allow OpenSSH → enable     pg_dump ... | gzip > backup.sql.gz
crontab -e  "0 3 * * *"        scp backup user@other:      certbot --nginx -d site.com
```

## D. Self-score

- 11+ of A → move on. 7–10 → redo lab + re-test tomorrow. <7 → re-read notes actively, redo lab.
