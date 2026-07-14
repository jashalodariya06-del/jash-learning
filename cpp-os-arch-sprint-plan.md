# C++ / OS / Computer Architecture — 8-Month Sprint Plan
### Sized for 2 hours/day (≈14 hrs/week) · ~32 weeks

This turns your roadmap into a week-by-week sprint you can actually run at 2 hrs/day.
The three tracks run **in parallel** (they reinforce each other), and every phase ends
with the roadmap's checkpoint so you prove you absorbed it before moving on.

> **Timeline:** ~32 weeks (≈7.5–8 months) at 14 hrs/week. If you ever get 3–4 hrs/day
> for a stretch, you compress toward the roadmap's 4–5 month full-time pace.

---

## How this sprint works

### The weekly engine (your default 14 hrs)

| Day | Focus | Hrs |
|-----|-------|-----|
| Mon | C++ — learn + code along | 2 |
| Tue | C++ — practice / build the checkpoint | 2 |
| Wed | Operating Systems | 2 |
| Thu | Computer Architecture | 2 |
| Fri | Spillover — finish whichever track's checkpoint is due | 2 |
| Sat | DSA problems (LeetCode / Striver) | 2 |
| Sun | Review the week + rest (light — flashcards, re-read notes) | 2 |

**Why C++ gets the most time:** it's the biggest track and the only one that needs heavy
hands-on coding. In months where **OS or Architecture is the heavier topic** (I flag these
below), move your Friday slot to that track instead.

### Three rules that make the hours count

1. **Cap input at ~1 hour.** Never watch/read for a full 2-hour block. Watch or read for
   up to an hour, then spend the rest of the session *writing code or solving problems*.
   You learn systems topics by building the toy version, not by watching someone else build it.
2. **Take notes in your own words.** One short `.md` file per topic. If you can't explain
   vtables / paging / cache mapping in a paragraph without notes, you haven't got it yet.
3. **Everything goes on GitHub.** Every checkpoint and capstone is a commit. Your repo *is*
   your resume for these roles.

---

## Master resource list (referenced throughout — set these up once)

**C++**
- 📺 **The Cherno — "C++" playlist** (`youtube.com/@TheCherno`) — the go-to visual course; great for "how it actually works under the hood" (pointers, memory, vtables, move semantics).
- 📖 **learncpp.com** — the best free structured text reference. Use it as your backbone; read the chapter, then watch Cherno on the same topic for intuition.
- 📺 **freeCodeCamp "C++ Programming Course – Beginner to Advanced" (Daniel Gakwaya, ~31 hrs)** (`youtube.com/@freecodecamp`) — full alternative course if you prefer one long guided track.

**Operating Systems**
- 📺 **Gate Smashers — Operating System (complete playlist)** (`youtube.com/@GateSmashers`) — concise, interview/numerical-focused; ideal for placement prep. Your primary OS video source.
- 📺 **Neso Academy — Operating Systems** (`youtube.com/@nesoacademy`) — more detailed/structured; use for depth on any topic Gate Smashers rushes.
- 📺 **CodeVault** (`youtube.com/@CodeVault`) & **Jacob Sorber** (`youtube.com/@JacobSorber`) — the best hands-on C playlists for `fork`/`exec`/pipes/`pthreads`/semaphores. Use these for OS *coding* checkpoints.
- 📖 **OSTEP — "Operating Systems: Three Easy Pieces"** (free at `ostep.org`) — genuinely the best self-study OS book; use instead of / alongside Silberschatz.

**Computer Architecture**
- 📺 **Neso Academy — Computer Organization & Architecture (COA)** (`youtube.com/@nesoacademy`) — GATE-oriented with tons of solved numericals (cache, AMAT, pipelining) that map exactly to your checkpoints. Primary source.
- 📺 **Gate Smashers — COA** (`youtube.com/@GateSmashers`) — concise alternative for quick revision.
- 📖 **Patterson & Hennessy — *Computer Organization and Design*, RISC-V edition** — the roadmap's pick; very approachable. Read the datapath/pipelining/cache chapters.

**DSA (ramps up hard in Months 7–8)**
- 📖 **Striver's A2Z DSA Sheet / SDE Sheet — takeuforward** (`takeuforward.org`) — the standard India-placement roadmap.
- 📺 **NeetCode 150** (`neetcode.io` / `youtube.com/@NeetCode`) — best pattern-based problem explanations.
- 🧩 **LeetCode** — solve here; **Codeforces** Div2 A/B for extra sharpness.

**Foundations tooling**
- 📺 **MIT "The Missing Semester of Your CS Education"** (`missing-semester.mit.edu`) — shell, git, tooling. Watch the shell + git lectures.

---

## PHASE 0 — Foundations (Weeks 1–2)

**Goal:** working Linux/C++ toolchain + number-system fluency. Don't skip even if you code —
the number-representation stuff shows up in interviews and in the Architecture track.

### Week 1 — Environment + number systems
- Set up **Linux** (native Ubuntu, or **WSL2** on Windows) + **VS Code**. Install `g++`, `make`, `git`.
- Learn shell basics (`cd ls mkdir rm cat grep`), then `g++` compile, a minimal `Makefile`, `git init/add/commit/push`.
- Number systems: binary ↔ hex, **two's complement**, **IEEE 754** float representation.
- **Learn from:** Missing Semester (shell + git lectures) · Neso Academy "Number System" videos · search *"IEEE 754 floating point representation explained"* for one focused explainer.

### Week 2 — C++ toolchain + first multi-file build
- Compilation model: **preprocessor → compiler → linker**; headers (`.h`) vs source (`.cpp`); why we split files.
- Write a 2–3 file program (`main.cpp` + a helper module) and build it with a `Makefile`.
- **Learn from:** The Cherno vids "How C++ Works", "How the Compiler Works", "How the Linker Works" · learncpp.com ch. 0–2.
- ✅ **Checkpoint:** Compile & run a multi-file C++ program via `g++` + a simple `Makefile`. Push it to a fresh GitHub repo.

---

## PHASE 1 — Month 1 (Weeks 3–6)
**C++ Core → start OOP · OS Fundamentals + Processes · Arch: Digital Logic + ISA**

### Week 3 — C++ core I + OS fundamentals
- **C++:** data types, operators, control flow, functions (overloading, default args, **pass by value / reference / pointer**). *learncpp ch. 1–8.*
- **OS:** what an OS does, **kernel vs user mode**, **system calls vs library calls**. *Gate Smashers OS L1–L10.*
- **Sat DSA:** arrays warm-up — 3–4 LeetCode easy.

### Week 4 — C++ pointers (the big one) + Arch digital logic
- **C++:** arrays, `std::string`, `std::vector`, then **pointers & references** — spend real time here, this is *the* concept to nail. Structs, enums. *learncpp ch. 9–12; Cherno "Pointers", "References".*
- **Arch:** logic gates, combinational vs sequential, flip-flops/registers/counters, K-maps — move fast, it's ECE review. *Neso Academy Digital Electronics (skim) or Gate Smashers Digital Logic.*
- **OS:** process vs thread, process states, **PCB**. *Gate Smashers process management.*

### Week 5 — C++ core wrap + CLI project + OS processes hands-on
- **C++:** finish core; **build the CLI inventory manager** (Stage-1 checkpoint) using only Stage-1 concepts.
- **OS:** context switching (mechanism + cost); **`fork()` / `exec()` / `wait()` hands-on in C on Linux.** *CodeVault processes playlist; Jacob Sorber process videos.*
- **Arch:** **ISA** — CPU registers, ALU, control unit, instruction formats, addressing modes, **RISC vs CISC**. *Neso Academy COA intro.*
- ✅ **C++ Checkpoint:** CLI text-based inventory manager.

### Week 6 — C++ OOP start + OS IPC + Arch assembly
- **C++:** classes, constructors/destructors, `this`, encapsulation. *learncpp classes chapters; Cherno OOP videos.*
- **OS:** threads (user vs kernel), `pthread` basics; **IPC overview** — pipes, shared memory, message queues. *CodeVault pipes + pthreads.*
- **Arch:** assembly basics — pick **RISC-V**; write and hand-trace a tiny program.
- ✅ **OS Checkpoint:** C program that `fork`s a child and communicates with it via a **pipe**.
- ✅ **Arch Checkpoint:** hand-trace a small assembly program (register/memory state after each instruction).

---

## PHASE 2 — Month 2 (Weeks 7–10)
**C++ Memory Management (interview-critical) · OS Scheduling · Arch: Datapath & Pipelining**

### Week 7 — C++ OOP depth
- Inheritance, **polymorphism, virtual functions, vtables** (know the under-the-hood layout), abstract classes/interfaces, operator overloading, **RAII**. *Cherno "Virtual Functions", "Interfaces"; learncpp inheritance + virtual chapters.*
- ✅ **OOP Checkpoint:** `Shape → Circle/Rectangle` hierarchy with virtual functions; **explain the vtable layout on paper.**

### Week 8 — C++ memory: stack/heap + smart pointers
- Stack vs heap, `new`/`delete`, **memory leaks, dangling pointers**, smart pointers: `unique_ptr` / `shared_ptr` / `weak_ptr`. *Cherno "Smart Pointers", "Stack vs Heap"; learncpp ch. 22.*
- **OS (this month is scheduling-heavy — use your Fri slot here too):** scheduling goals (throughput/latency/fairness); FCFS, SJF, Round Robin, Priority, Multilevel Queue; starvation & aging. *Gate Smashers CPU scheduling (great numericals).*

### Week 9 — C++ Rule of 3/5 + move semantics + Arch datapath
- Rule of 3 / Rule of 5, **move semantics**, `std::move`, rvalue references. *Cherno "Move Semantics", "lvalues and rvalues".*
- **Arch:** single-cycle vs multi-cycle datapath. *Neso Academy datapath; P&H ch. 4.*

### Week 10 — C++ RAII wrapper + scheduling sim + pipelining
- **C++:** build the **custom `unique_ptr`-like RAII wrapper** (Stage-3 checkpoint).
- **OS:** code the **scheduling simulator** (2–3 algorithms) — compare avg waiting/turnaround.
- **Arch:** **pipelining** — 5 stages (IF/ID/EX/MEM/WB); hazards (structural/data/control) and fixes (forwarding, stalling, branch prediction). *Neso Academy pipelining + hazards.*
- ✅ **C++ Checkpoint:** custom `unique_ptr`-like RAII wrapper.
- ✅ **OS Checkpoint:** simulate 2–3 scheduling algorithms in C++; compare metrics.
- ✅ **Arch Checkpoint:** trace instructions through a 5-stage pipeline; identify hazards on paper.

---

## PHASE 3 — Month 3 (Weeks 11–14)
**C++ STL & Modern C++ · OS Synchronization (heavily tested) · Arch: Memory Hierarchy**

> Do the **Arch cache** topics and **OS virtual-memory** intuition close together — they're the same story from two sides.

### Week 11 — STL containers + OS critical section
- **C++:** `vector`, `map`, `unordered_map`, `set`, `deque`, `stack`, `queue`; iterators. *learncpp STL chapters; Cherno "Vector", "Iterators".*
- **OS:** critical-section problem, **mutexes, semaphores, monitors**. *Gate Smashers synchronization.*

### Week 12 — STL algorithms + classic sync problems
- **C++:** `<algorithm>` — `sort`, `find`, `accumulate`, etc.; lambdas + `std::function`.
- **OS:** classic problems — **Producer-Consumer, Readers-Writers, Dining Philosophers**; deadlocks (4 conditions, prevention, avoidance/**Banker's Algorithm**, detection). *Gate Smashers deadlocks + classic problems; CodeVault semaphores for the coding side.*

### Week 13 — Templates + Arch caches
- **C++:** function & class templates, a taste of template metaprogramming. *Cherno "Templates".*
- **Arch:** cache basics — direct-mapped / set-associative / fully associative; hit/miss; write-through vs write-back; L1/L2/L3; **locality (temporal/spatial)**. *Neso Academy cache mapping + solved numericals.*

### Week 14 — Modern C++ + sync coding + cache numericals
- **C++:** C++11/14/17/20 essentials — `auto`, structured bindings, `constexpr`, ranges (17/20 basics).
- **OS:** code **Producer-Consumer + Dining Philosophers** with `pthread` mutexes/semaphores.
- **Arch:** cache hit/miss + AMAT calculations.
- ✅ **C++ Checkpoint:** solve **30–40 LeetCode easy/medium** using STL idiomatically (spread over the phase).
- ✅ **OS Checkpoint:** Producer-Consumer & Dining Philosophers with pthreads.
- ✅ **Arch Checkpoint:** compute hit/miss rate + average access time for a given config + access pattern.

---

## PHASE 4 — Month 4 (Weeks 15–18)
**C++ Concurrency · OS Memory Management · Arch: I/O, Interrupts, Parallelism**

### Week 15 — C++ threads + OS address spaces
- **C++:** `std::thread`, mutexes, locks, condition variables. *Cherno "Threads"; cppreference for `std::mutex`/`condition_variable`.*
- **OS:** logical vs physical addresses, **paging, segmentation**. *Gate Smashers memory management; OSTEP paging chapters.*

### Week 16 — C++ race conditions/deadlocks + OS page tables
- **C++:** race conditions, deadlocks, **atomic operations**; `std::async`, futures/promises (overview).
- **OS:** page tables, **TLB**, page replacement (FIFO, LRU, Optimal). *Gate Smashers page replacement.*

### Week 17 — C++ exception safety + OS virtual memory + Arch I/O
- **C++:** exception handling & exception-safety guarantees; compilation deep-dive (static vs dynamic linking, undefined behavior, `const`/`constexpr`/`volatile`).
- **OS:** **virtual memory, demand paging, thrashing**, internal/external fragmentation.
- **Arch:** interrupts vs polling, interrupt-handling flow, **DMA**, buses/I/O interfacing. *Neso Academy I/O organization.*

### Week 18 — Concurrency + page-replacement + parallelism
- **C++:** build the **multithreaded producer-consumer queue** with proper synchronization.
- **OS:** implement **LRU + FIFO page replacement**; compare page-fault counts on a reference string.
- **Arch:** multicore basics, **cache coherence (MESI overview)**, **Amdahl's Law**.
- ✅ **C++ Checkpoint:** multithreaded producer-consumer queue.
- ✅ **OS Checkpoint:** LRU + FIFO page replacement in C++; compare page faults.

---

## PHASE 5 — Month 5 (Weeks 19–22) — Consolidate + first capstone
**Tie the tracks together and build. This is where you turn knowledge into resume items.**

### Week 19 — OS File Systems & I/O
- File-system structure, **inodes**, directory structures; disk scheduling (FCFS, SCAN, C-SCAN, SSTF); polling vs interrupts vs DMA (connects to Arch). *Gate Smashers file systems + disk scheduling.*

### Week 20 — The unifying idea: performance = memory behavior
- Understand **why row-major array traversal beats column-major** (cache lines + spatial locality). Write a benchmark in C++ that measures it — this single demo unifies all three tracks and is a great interview talking point.
- **Learn from:** re-watch Cherno "How C++ Works" + Neso cache locality with this lens.

### Weeks 21–22 — 🛠️ Capstone #1
Pick the one that best fits your target role and build it end-to-end:
- **A simple shell** (`fork`/`exec`/`wait`, pipes, redirection) — best C++ + OS tie-in, and the strongest single resume item for systems/embedded.
- *or* **A cache simulator** (memory trace → hit/miss for different configs) — best Architecture + C++ tie-in.

---

## PHASE 6 — Month 6 (Weeks 23–26) — Second capstone + fundamentals review
- **Weeks 23–24:** 🛠️ **Capstone #2** — pick a *different* track pairing than Capstone #1:
  - **Multithreaded memory allocator** (custom `malloc`/`free` with a free list) — C++ + OS memory.
  - **CPU scheduler simulator** with a Gantt-chart visualizer — OS + C++.
  - **Key-value store with LRU eviction** — DSA + OS + systems-design crossover (very strong resume line).
- **Weeks 25–26:** **Job-ready review across all three tracks.** Build a one-page cheat sheet per track. Practice explaining out loud: **vtables, RAII, smart pointers, move semantics** (C++); **what happens from `int main()` to program exit** — loader, stack setup, syscalls, exit (OS); **cache numericals + pipeline hazards + AMAT** (Arch).

---

## PHASE 7 — Months 7–8 (Weeks 27–32) — DSA grind + mock interviews

Now DSA takes the wheel. Shift your weekly split to **~8–10 hrs DSA**, ~4 hrs review/mocks.

| Week | DSA focus (Striver A2Z / NeetCode 150) | Alongside |
|------|----------------------------------------|-----------|
| 27 | Arrays, strings, two-pointers, sliding window | CS-fundamentals flashcards daily |
| 28 | Hashing, stacks/queues, linked lists | OS numericals under time pressure |
| 29 | Recursion, backtracking, binary search | Arch numericals under time pressure |
| 30 | Trees + BST, heaps | 1 mock interview |
| 31 | Graphs (BFS/DFS, topo, shortest paths) | 1 mock interview |
| 32 | Dynamic programming + full revision | 2 mock interviews + resume polish |

**Target:** **150+ problems** total (you'll have ~40–70 banked from earlier phases). Redo every
problem you couldn't solve unaided. Do mocks with a peer or on Pramp/interviewing.io style platforms.

---

## Capstone shortlist (build 2–3 across Phases 5–6)

1. **Simple shell** — `fork`/`exec`/`wait`, pipes, redirection *(C++ + OS)*
2. **Multithreaded memory allocator** — custom `malloc`/`free` + free list *(C++ + OS memory)*
3. **Cache simulator** — memory trace → hit/miss across configs *(Arch + C++)*
4. **CPU scheduler simulator** — Gantt-chart output *(OS + C++)*
5. **Key-value store with LRU eviction** — *(DSA + OS + systems design)* ← strongest resume line

For each: write a short README with **design decisions + tradeoffs**. Interviewers ask "why did you build it that way?" more than "what does it do?"

---

## Final interview-prep checklist

- [ ] 150+ DSA problems solved in C++ (arrays, strings, trees, graphs, DP, sliding window)
- [ ] Can explain vtables, RAII, smart pointers, move semantics **without notes**
- [ ] Can solve deadlock / scheduling / paging numericals under time pressure
- [ ] Can compute cache hit rate / AMAT and explain pipeline hazards
- [ ] Built ≥2 capstones and can explain the design tradeoffs
- [ ] Comfortable with `git`, Linux CLI, reading a `Makefile` / `CMakeLists.txt`
- [ ] Mock interviews done (peer or platform) covering DSA + CS fundamentals

---

## Progress tracker (tick as you clear each checkpoint)

- [ ] **P0** Multi-file program builds with `g++` + Makefile (on GitHub)
- [ ] **P1** CLI inventory manager · fork+pipe C program · assembly hand-trace
- [ ] **P2** vtable/shape hierarchy · RAII smart-pointer wrapper · scheduler sim · pipeline hazard trace
- [ ] **P3** 30–40 STL problems · Producer-Consumer + Dining Philosophers · cache AMAT numerical
- [ ] **P4** Multithreaded PC queue · LRU+FIFO page replacement
- [ ] **P5** Capstone #1 shipped · row-major vs column-major benchmark
- [ ] **P6** Capstone #2 shipped · three-track cheat sheets
- [ ] **P7** 150+ DSA · 4+ mock interviews · resume ready

---

*Note: MOOC/video offerings shift over time. If a linked channel's playlist has been
reorganized when you reach it, search the channel for the topic name — the topic list above
stays valid regardless of which specific video covers it.*
