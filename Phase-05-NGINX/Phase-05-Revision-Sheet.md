# Phase 05 — Revision Sheet (Active Recall)

> Do NOT open the notes. Answer aloud/on paper, then check and mark ✅/❌. Re-test ❌ items tomorrow.
> Review: after phase → +1 day → +3 days → +1 week → +1 month.

## A. Rapid-fire recall

1. What is NGINX? What was the C10K problem and how does NGINX's architecture solve it?
2. Forward proxy vs reverse proxy — who does each hide? Which is NGINX's main role here?
3. List 5 "front door" jobs NGINX does better than Spring Boot.
4. What is TLS termination? 3 reasons to terminate at NGINX instead of the app.
5. How does one NGINX serve many domains on one IP? (which header, which directive?)
6. The safe config-change workflow — 4 commands in order. Why `reload` over `restart`?
7. Recite a minimal reverse-proxy server block (proxy_pass + the 4 proxy_set_header lines).
8. Why do Host / X-Forwarded-For / X-Forwarded-Proto matter? What breaks without them?
9. 502 vs 504 behind NGINX — root cause of each, and the 3 checks for a 502.
10. Where are access.log and error.log, and what does each contain?
11. How does certbot/Let's Encrypt prove you own the domain? What does certbot change in your config?
12. Recite the HTTP→HTTPS redirect server block.
13. What do these do: HSTS header, X-Frame-Options, server_tokens off?
14. Rate limiting: what do `limit_req_zone rate=10r/s` and `burst=20` mean?
15. What causes a 413 error on uploads and the fix?
16. Static files: which location block pattern + headers make browsers cache assets 30 days?

## B. Write from memory

- Full production server block: api.shop.com, HTTPS + redirect, proxy to :8080, forwarding headers, rate limit, gzip, 20MB uploads.
- The request path for `/product.png` vs `/api/products` through your config.

## C. Command drill

```
nginx -t                    systemctl reload nginx        tail -f /var/log/nginx/error.log
certbot --nginx -d site.com certbot renew --dry-run       ln -s sites-available/x sites-enabled/
```

## D. Self-score

- 13+ of A → move on. 8–12 → redo lab + re-test tomorrow. <8 → re-read notes actively, redo lab.
