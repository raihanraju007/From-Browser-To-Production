# Phase 04 — Revision Sheet (Active Recall)

> Do NOT open the notes. Answer aloud/on paper, then check and mark ✅/❌. Re-test ❌ items tomorrow.
> Review: after phase → +1 day → +3 days → +1 week → +1 month.

## A. Rapid-fire recall

1. Why is Linux (Ubuntu LTS) the server standard? What does LTS mean?
2. Where do you look for: configuration? logs? your app? (3 directories)
3. Decode `-rwxr-x--- 1 deploy www-data app.jar` completely. What's the chmod number?
4. What are 644, 755, 600 used for? Why must SSH private keys be 600?
5. Why run apps as a dedicated non-root user? What principle is that?
6. How do SSH keys work (tie to Phase 3 crypto)? Which file goes to the server?
7. The 2 sshd_config hardening lines — what are they?
8. `kill` vs `kill -9` — what's the difference and which first?
9. Why is `nohup app &` wrong for production? What replaces it?
10. Recite the systemd unit file sections and the 5 most important directives (User, ExecStart, Restart, After, WantedBy).
11. The 4-command debugging ritual when a service is down.
12. `journalctl -u app -f` vs `/var/log/` files — what lives where? What is auth.log for?
13. The ufw setup order — which rule MUST come first and why?
14. Which ports open on a web server? Why NOT 5432/8080?
15. Full disk took the DB down — which two commands find the culprit?
16. Recite the L3→L4→L7 server debugging ladder with commands.

## B. Write from memory

- A complete systemd unit for `shop-api.jar` in `/opt/shop`, user `shopuser`, prod profile, auto-restart, after PostgreSQL.
- The first-30-minutes checklist for a fresh server (order matters).

## C. Command drill — what does each do?

```
systemctl status app     journalctl -u app --since "10 min ago"    systemctl enable app
ss -tulpn                ufw allow OpenSSH                          chmod 600 ~/.ssh/id_ed25519
ps aux | grep java       df -h / du -sh /var/log/*                  ssh-copy-id user@host
```

## D. Self-score

- 13+ of A → move on. 8–12 → redo lab + re-test tomorrow. <8 → re-read notes actively, redo lab.
