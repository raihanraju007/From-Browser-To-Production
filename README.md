# From Browser to Production 📚

My learning notes: the complete journey of a request from a user's browser to a production server.

```
User Browser → DNS → Internet → Firewall → Load Balancer → NGINX
→ Application Server → Spring Boot API → Database → Cache → Response → Browser
```

## The learning method (why this structure)

Re-reading notes is one of the **least** effective study techniques. This course uses what actually works — **active recall + spaced repetition + hands-on labs**:

Each phase folder contains exactly two documents (each as `.md` + `.pdf`):

- **`Phase-XX-Notes`** — the full chapter: explanations, analogies, diagrams, commands, mistakes, best practices, interview questions, LAB, and the ASSIGNMENT.
- **`Phase-XX-Revision-Sheet`** — questions ONLY, no answers. You answer from memory, then check yourself against the notes.

### The study loop per phase

```
1. READ the notes once (don't highlight, don't re-read)
2. DO the lab hands-on — typing, breaking, fixing
3. RECALL: take the Revision Sheet closed-book, score yourself
4. SOLVE the assignment → submit to Claude for review/exam
5. SPACED REVIEW: retake the Revision Sheet after 1 day, 3 days, 1 week, 1 month
   (only re-read the notes sections you failed)
```

Only move to the next phase after step 4 passes.

## Roadmap & Progress

| Phase | Topic | Notes | Revision | Status |
|-------|-------|-------|----------|--------|
| 00 | Linux & Terminal Basics | [Notes](Phase-00-Linux-Basics-Prerequisites/Phase-00-Notes.md) | [Sheet](Phase-00-Linux-Basics-Prerequisites/Phase-00-Revision-Sheet.md) | ⬜ |
| 01 | Internet Fundamentals | [Notes](Phase-01-Internet-Fundamentals/Phase-01-Notes.md) | [Sheet](Phase-01-Internet-Fundamentals/Phase-01-Revision-Sheet.md) | 🔄 |
| 02 | DNS and Domains | [Notes](Phase-02-DNS-and-Domains/Phase-02-Notes.md) | [Sheet](Phase-02-DNS-and-Domains/Phase-02-Revision-Sheet.md) | ⬜ |
| 03 | HTTP and HTTPS | [Notes](Phase-03-HTTP-and-HTTPS/Phase-03-Notes.md) | [Sheet](Phase-03-HTTP-and-HTTPS/Phase-03-Revision-Sheet.md) | ⬜ |
| 04 | Linux Server Administration | [Notes](Phase-04-Linux-Server-Administration/Phase-04-Notes.md) | [Sheet](Phase-04-Linux-Server-Administration/Phase-04-Revision-Sheet.md) | ⬜ |
| 05 | NGINX Deep Learning | [Notes](Phase-05-NGINX/Phase-05-Notes.md) | [Sheet](Phase-05-NGINX/Phase-05-Revision-Sheet.md) | ⬜ |
| 06 | Docker and Containers | [Notes](Phase-06-Docker-and-Containers/Phase-06-Notes.md) | [Sheet](Phase-06-Docker-and-Containers/Phase-06-Revision-Sheet.md) | ⬜ |
| 07 | VPS and Deployment | [Notes](Phase-07-VPS-and-Deployment/Phase-07-Notes.md) | [Sheet](Phase-07-VPS-and-Deployment/Phase-07-Revision-Sheet.md) | ⬜ |
| 08 | AWS Cloud | [Notes](Phase-08-AWS-Cloud/Phase-08-Notes.md) | [Sheet](Phase-08-AWS-Cloud/Phase-08-Revision-Sheet.md) | ⬜ |
| 09 | Scaling and Architecture | [Notes](Phase-09-Scaling-and-Architecture/Phase-09-Notes.md) | [Sheet](Phase-09-Scaling-and-Architecture/Phase-09-Revision-Sheet.md) | ⬜ |
| 10 | Load Balancing | [Notes](Phase-10-Load-Balancing/Phase-10-Notes.md) | [Sheet](Phase-10-Load-Balancing/Phase-10-Revision-Sheet.md) | ⬜ |
| 11 | Kubernetes | [Notes](Phase-11-Kubernetes/Phase-11-Notes.md) | [Sheet](Phase-11-Kubernetes/Phase-11-Revision-Sheet.md) | ⬜ |
| 12 | Final Production Project | [Notes](Phase-12-Final-Production-Project/Phase-12-Notes.md) | [Final Exam](Phase-12-Final-Production-Project/Phase-12-Revision-Sheet.md) | ⬜ |

Legend: ⬜ not started · 🔄 in progress · ✅ notes+lab+recall done · 🏆 assignment passed

## Assignment & spaced-review tracker

| Phase | Assignment passed | +1 day | +3 days | +1 week | +1 month |
|-------|-------------------|--------|---------|---------|----------|
| 00 | | | | | |
| 01 | | | | | |
| 02 | | | | | |
| 03 | | | | | |
| 04 | | | | | |
| 05 | | | | | |
| 06 | | | | | |
| 07 | | | | | |
| 08 | | | | | |
| 09 | | | | | |
| 10 | | | | | |
| 11 | | | | | |
| 12 | | | | | |

*(Started: 2026-07-19)*
