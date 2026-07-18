# Phase 11 — Revision Sheet (Active Recall)

> Do NOT open the notes. Answer aloud/on paper, then check and mark ✅/❌. Re-test ❌ items tomorrow.
> Review: after phase → +1 day → +3 days → +1 week → +1 month.

## A. Rapid-fire recall

1. Which 4 questions explode when you go from one machine (compose) to many? What is K8s in one sentence?
2. Declarative vs imperative — what does "reconciliation loop" mean?
3. Control plane components (API server, etcd, scheduler, controllers) — one line each. Node components (kubelet, kube-proxy, runtime)?
4. Pod vs Deployment vs ReplicaSet — roles and relationship. Why never create bare pods?
5. Why are pods "mortal cattle"? What churns every time one is rescheduled?
6. Readiness vs liveness probe — what does each gate? Consequence of each failing?
7. Why must liveness NOT check the database? (name the failure mode)
8. `resources.requests` vs `limits` — who uses each (scheduler? kill/throttle?)?
9. What is a Service? Which problem over mortal pods? How does in-cluster DNS naming work?
10. ClusterIP vs NodePort vs LoadBalancer vs Ingress — when each?
11. ConfigMap vs Secret — and the truth about Secret's "encryption"?
12. Ingress + NGINX Ingress Controller — the full path from Internet to pod (5 hops). Where does TLS come from (cert-manager)?
13. Rolling update: what happens pod-by-pod? The rollback command?
14. HPA vs Cluster Autoscaler — what does each scale? Which Phase-9 property makes HPA safe?
15. Recite the debug decision tree: Pending / ImagePullBackOff / CrashLoopBackOff / Running-but-unreachable.
16. The JVM + memory limits trap — what happens and the container-aware fix?
17. When is K8s the WRONG choice? (the $200-cluster-vs-$6-VPS argument)

## B. Write from memory

- Deployment YAML skeleton: 3 replicas, image tag, both probes, resources, envFrom.
- Service YAML matching it (selector! ports!).
- The command sequence: deploy new version → watch rollout → roll back.

## C. Command drill

```
kubectl get pods -o wide        kubectl describe pod X (what's at the bottom?)
kubectl logs -f deploy/api --previous          kubectl get endpoints (what bug does it reveal?)
kubectl rollout undo deploy/api                kubectl autoscale deploy api --min=3 --max=15 --cpu-percent=70
kubectl port-forward svc/api 8080:80           kubectl apply -f k8s/
```

## D. Self-score

- 14+ of A → move on. 9–13 → redo lab + re-test tomorrow. <9 → re-read notes actively, redo lab.
