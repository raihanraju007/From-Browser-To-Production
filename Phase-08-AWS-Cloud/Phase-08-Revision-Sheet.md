# Phase 08 — Revision Sheet (Active Recall)

> Do NOT open the notes. Answer aloud/on paper, then check and mark ✅/❌. Re-test ❌ items tomorrow.
> Review: after phase → +1 day → +3 days → +1 week → +1 month.

## A. Rapid-fire recall

1. What is "the cloud" in one sentence? The 3 reasons companies pay more than VPS prices?
2. Region vs Availability Zone — and why production = at least 2 AZs?
3. "Cattle, not pets" — what does it mean concretely?
4. IAM: user vs role vs policy vs group. How does an EC2 app get S3 access WITHOUT keys — and what does the SDK actually receive?
5. Two rules about the root account?
6. EC2 vocabulary: instance, AMI, key pair, user data, Elastic IP — why Elastic IP for DNS?
7. Security groups: default inbound stance? What does "source = another SG" enable? Recite the web→app→db SG chain.
8. VPC: what makes a subnet "public" vs "private" (the exact mechanism)?
9. IGW vs NAT Gateway — who uses each and in which direction? (Phase-1 NAT link)
10. Which tier lives in private subnets and why is that stronger than a ufw rule?
11. RDS vs postgres-on-EC2 — what are you buying? Multi-AZ vs read replica (the classic distinction!)?
12. S3: object storage vs filesystem? Which Phase-9 problem does it solve? Default bucket visibility?
13. CloudFront: edge location, cache hit vs miss, why it beats physics for Dhaka→US.
14. Route 53: what's an alias record (which Phase-2 limitation does it fix)? Name 3 routing policies.
15. CloudWatch: metrics vs logs vs alarms — one production alarm example for each of ALB/RDS/billing.
16. The 3 most common surprise-bill sources? What do you set up FIRST in a new account?

## B. Write / draw from memory

- The full VPC diagram: CIDR, 2 public + 2 private subnets across AZs, IGW, NAT, route tables, where ALB/EC2/RDS sit.
- The Local → VPS → AWS comparison table (at least 8 rows).

## C. Command drill

```
aws s3 cp backup.sql.gz s3://bucket/     aws s3 sync ./dist s3://frontend
ssh -i key.pem ubuntu@elastic-ip         nc -zv rds-endpoint 5432 (from where does it work?)
```

## D. Self-score

- 13+ of A → move on. 8–12 → redo lab + re-test tomorrow. <8 → re-read notes actively, redo lab.
