# Phase 03 — Revision Sheet (Active Recall)

> Do NOT open the notes. Answer aloud/on paper, then check and mark ✅/❌. Re-test ❌ items tomorrow.
> Review: after phase → +1 day → +3 days → +1 week → +1 month.

## A. Rapid-fire recall

1. What is HTTP, which OSI layer, and what does it ride on?
2. Write the 4 parts of a raw HTTP request from memory (request line, headers, blank line, body).
3. GET / POST / PUT / PATCH / DELETE — meaning of each; which are idempotent?
4. What does idempotent mean, and why does it matter for retries? Give the payments example.
5. Status codes from memory: 200, 201, 204, 301, 302, 304, 400, 401, 403, 404, 409, 429, 500, 502, 503, 504.
6. 401 vs 403? 502 vs 504 — and WHICH component typically produces 502/504?
7. What is the `Host` header for, and which big NGINX feature depends on it?
8. What are `X-Forwarded-For` and `X-Forwarded-Proto`, and who adds them?
9. "HTTP is stateless" — what does that mean, and why is it a scaling feature?
10. Explain the cookie-session login flow (4 steps). Where does the session live?
11. Cookie flags: HttpOnly, Secure, SameSite — what does each protect against?
12. JWT vs server-side session — trade-offs (scaling vs revocation).
13. The 3 attacks plain HTTP allows; the 3 guarantees HTTPS gives.
14. Symmetric vs asymmetric encryption — speed, key setup, and how TLS combines them.
15. What is a certificate? What exactly does the browser verify? What is a CA?
16. Recite the TLS handshake steps (Hello → cert → verify → key exchange → encrypted).
17. What is forward secrecy? What can a network observer STILL see with HTTPS?
18. Order the full journey: DNS → ? → ? → ? for `https://example.com`.

## B. Draw / write from memory

- REST endpoint table for orders (list/create/get/replace/delete) with methods, paths, success codes.
- The TLS handshake as a 6-line dialogue between Browser and Server.

## C. Command drill — what does each do?

```
curl -v https://example.com     curl -i URL        curl -I URL
curl -X POST -H "Content-Type: application/json" -d '{...}' URL
openssl s_client -connect host:443 ... | openssl x509 -noout -dates
nc localhost 8000   (then type a raw GET request)
```

## D. Self-score

- 14+ of A → move on. 9–13 → redo lab + re-test tomorrow. <9 → re-read notes actively, redo lab.
