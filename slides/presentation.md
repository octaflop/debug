---
marp: true
title: Python Web Development Journey
theme: gaia
paginate: true
---

# Debugging
## Stories from python and beyond

---

# Stories

---

### Chris!

9m lines c++
20 year old, young careers

Week after release no one could reproduce anything.
Reviews were unkind. A lot of bad press.
Users were advocating to use previous version.
Swat team of 3 took 4 weeks to reproduce issue. After a couple weeks found a “pointer truncation” issue.
Solution: Forced virtual memory allocation. Used tool to view memory layout.
Wrote utility to allocate memory and fill in all the gaps until everything was full and everything to flush out crashes.

---

## Faris

90k tests and permutations which had 100+ versions and updates associated. Batch job was 72hours.
Very touchy, just run it and let it run. For whatever reason if it ran to hour 70 it meant it had to be reran.
Created observation metrics for how to. Looking at SQL query explain of a query that took 15min just to explain.
Epilogue; true root cause: cloud team was killing jobs they didn’t understand why the just killed it.


---


## Bruce

Hardware bug. Multiple 32bit processors. Colab with Motorola.
You had flexibility to single step the process. It wasn’t limited to just run.
SE had a process that would crash and only way to get it back is via power cycling the machine.
5 modes available that used 3 bits. Was in a mode that didn’t exist. Creator had not covered unused modes.

Could tell the processor wasn’t in a valid mode. It had to be the state machine based on the invalid mode and very limited ways that could happen. Random noise and proper recovery seemed to be the result.

---


## Ty

Stress testing system and ended up getting an error that was nonreplicable. Realized it was using a stale cache and tricky race condition and first deep dive into debugging.




---

# Lessons  🎯

- Stay Organized
- Build a test environment
- Chop off the parts that don't matter
  - Be modular
- Write code for your future self
- Test one variable at a time: be scientific
- Communicate
- State upfront assumptions and hold to that
- PEP8 / type hinting
  - reproducibility matters
- test the code you think you're testing
  - stg / dev / local web indications
  - versions
  - while we're on this: update should be built in
- `git bisect`

---

# Resources 📚


---

# Workshop Repository

- [debug](https://github.com/octaflop/debug)
- Contains all examples and additional resources
- ![](./repo_qr.png)