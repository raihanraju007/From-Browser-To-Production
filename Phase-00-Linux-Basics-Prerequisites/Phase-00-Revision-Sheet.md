# Phase 00 — Revision Sheet (Active Recall)

> **How to use:** do NOT open the notes. Answer aloud or on paper. Then check against the notes and mark ✅/❌. Re-test only the ❌ items the next day.
> **Review schedule:** after finishing the phase → next day → after 3 days → after 1 week → after 1 month.

## A. Rapid-fire recall (say the answer out loud)

1. Kernel vs distro vs shell vs terminal — one line each.
2. What do `.`, `..`, `~`, `/` mean in a path? Absolute vs relative path?
3. What's the difference between `cat`, `less`, `head`, `tail`, `tail -f`?
4. What does the pipe `|` do? What do `>`, `>>`, `2>`, `2>&1` do?
5. Which command searches text inside files? Inside a whole folder recursively?
6. Which command finds files by name?
7. What is `$PATH` and what happens when you type a command name?
8. How do you set an environment variable for one session? Permanently?
9. What does `sudo` do, and when should you NOT use it?
10. `apt update` vs `apt upgrade` — difference?
11. How do you save and exit nano? How do you escape vim?
12. What do Ctrl+C, Ctrl+R, Ctrl+L, Tab do?
13. Why is `rm -rf` dangerous? Is there a trash bin?
14. `df -h` vs `free -h` vs `du -sh` — what does each show?

## B. Draw / write from memory

- Write the one-liner: count lines containing "ERROR" in `app.log`.
- Write the one-liner: follow a log live AND only show lines with "500". *(hint: tail -f | grep)*
- Write the anatomy of a command: which part is the command, flags, argument in `ls -lah /var/log`?

## C. Command drill — what does each do? (then verify in a terminal)

```
mkdir -p a/b/c        cp -r dir1 dir2        mv old.txt new.txt
grep -rn "TODO" src/  find . -name "*.java"  history | grep ssh
ps aux | grep java    which java             wc -l file.txt
```

## D. Self-score

- 12+ of section A correct → move on.
- 8–11 → redo the lab, re-test tomorrow.
- <8 → re-read the notes actively (write your own summary), redo lab, re-test.
