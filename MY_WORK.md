# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers

> This is the **only file** your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be **in your own words**.

---

## 🛑 STOP: Read This Before You Do Anything Else

> ### 1️⃣ Read the whole `README.md` first
> The `README.md` in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. **If you skip it, you will lose marks.**
>
> ### 2️⃣ Understand the full code before answering any question
> Open `SchedulerSimulationSync.java` and read it **from top to bottom**. You must be able to explain what `SharedStats`, `ReadyQueue`, `CpuWorker`, `RaceWindow.pause()`, `ReentrantLock` and `Semaphore` do **before** you write a single answer in Parts B and C. **Run the original starter first** (it is intentionally broken) and **save its output**: you need it for Question 1 of Part C.
>
> ### 3️⃣ Use only the code of this repository
> Work **only** on `SchedulerSimulationSync.java` from this repository. Do **not** copy or paste code from your previous assignments.
>
> ### 4️⃣ Commit many times, not once
> A single commit, or all commits made in the last hour, costs you **-0.5 mark**. See the [Commit Rules](#-commit-rules-mandatory) below.

**How to use this file:**
1. Fill in your **Student Information** (below) right now.
2. Follow the steps in the **Work Roadmap** in order.
3. Update the **Development Log** *every time* you work on the assignment, not at the end.
4. Do not delete any section header. Replace the `[...]` placeholders with your own text.

---

## 👤 Student Information

> ⚠️ **WARNING:** Fill this in first. Your name and ID must match the student ID you set in `SchedulerSimulationSync.java` (line 304) and the one you say in your video.

| Field | Your Answer |
|-------|-------------|
| **Full Name** | [Motab barrak alosaimi] |
| **Student ID** | [445050134] |
| **University Email** | [445050134]@std.psau.edu.sa |
| **GitHub Username** | [Motab-alosimi-445] |
| **Repository Link** | [https://github.com/Motab-alosimi-445/OS-Assignment3-Motab-Alosaimi] |
 
---

## 🎥 Video Link

**Video Link**: [https://drive.google.com/file/d/1GcVORnmIWXyfpFmNE0dGSon8OkjYwM-B/view?usp=drive_link]

> ⚠️ **WARNING:** The video must be **publicly accessible** ("Anyone with the link can view") on **Google Drive**, **YouTube (Unlisted or Public)** or any other cloud file-sharing system. A private, restricted or broken link counts as a **missing video (-1 mark)**.
>
> 💡 **TIP:** Open the link in a **private/incognito window** before you submit. If it asks you to log in or request access, it is not public.
>
> 📌 **NOTE:** The link goes in **this file only** (`MY_WORK.md`), **not** in `README.md`. Name your video file `StudentID_Assignment3_Demo.mp4`. It must last **2 to 3 minutes**.

---

## 🗺️ Work Roadmap (follow in this order)

| Step | What to do | Where | Marks |
|:----:|------------|-------|:-----:|
| 0 | Read `README.md`, read the full code, **run the original starter and save its output** (it fails on purpose) | Your IDE | – |
| 1 | Fork, rename, keep the repo **PUBLIC**, set your student ID (line 304), **commit** | GitHub + code | Part 1 (1) |
| 2 | Feature 1: Mutex lock on the ready queue, **commit** | Code | Part 2 (0.25) |
| 3 | Feature 2: Mutex lock(s) on the shared statistics, **commit** | Code | Part 2 (0.25) |
| 4 | Feature 3: Counting semaphore instead of busy waiting, **commit** | Code | Part 2 (0.5) |
| 5 | Development Log (5+ entries, different dates) | This file, Part A | Part 3 (0.5) |
| 6 | Reflection (4 questions) | This file, Part B | Part 3 (0.5) |
| 7 | Technical Answers (4 questions) | This file, Part C | Part 3 (0.5) |
| 8 | Record the video, upload it, paste the link above | Video + this file | Part 4 (1.5) |
| 9 | Final check, then submit the repo link on Blackboard | Blackboard | – |

> 💡 **TIP:** Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

**Minimum: 4 meaningful commits. Aim for 7 or more.**

| # | Commit | Example message |
|:-:|--------|-----------------|
| 1 | Student ID set | `Set my student ID: 441234567` |
| 2 | Feature 1: Ready queue lock | `Feature 1: Protected the ready queue with a ReentrantLock` |
| 3 | Feature 2: Statistics locks | `Feature 2: Added locks to the shared statistics counters` |
| 4 | Feature 3: Semaphore | `Feature 3: Replaced busy waiting with a counting semaphore` |
| 5 | Development log entries | `Docs: Added development log entries 1-3` |
| 6 | Reflection and answers | `Docs: Completed reflection and technical answers` |
| 7 | Video link | `Docs: Added demo video link` |

**Rules:**
- ✅ **One commit per feature.** Do not put all three features in one commit.
- ✅ **Commit after each work session**, and after each part of this file.
- ✅ **Spread your commits over different dates.** Not all in one day.
- ❌ **Do not make all commits in the last hour** before the deadline (November 14, 2026).
- ❌ **No vague messages** like `done`, `update` or `final version`.

> 💡 **TIP:** Your commit history is checked and you **show it in your video** (at least 4 commits visible). Your development log dates should match your commit dates.
>
> 💡 **TIP:** **Use VS Code** (see *Recommended Development Environment* in `README.md` for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. **Pushing** matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)

> ⚠️ **WARNING:** Minimum **5 entries**, spread over **different dates**. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be **between the start of the assignment and the deadline (November 14, 2026)**.
>
> 💡 **TIP:** Write an entry at the **end of each work session**, while you still remember what happened. It takes 5 minutes.
>
> 💡 **TIP:** Be specific. "Worked on the code" is a weak entry. "Added a `ReentrantLock queueLock` to `ReadyQueue` and wrapped the body of `poll()` in `lock()` / `try` / `finally { unlock() }`" is a strong one.
>
> 📌 **NOTE:** Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

## Example Entry (do not copy it, write your own)

### Entry 1 - [November 2, 2026, 4:30 PM]
**What I did**: Forked the repository, set my student ID, and ran the original starter

**Details**:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked `P1`, then `IllegalThreadStateException` and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: `Set my student ID: 441234567`

**Challenges**: I did not understand why the same process was picked by three CPUs

**Solution**: Read `ReadyQueue.poll()` again and found the `RaceWindow.pause()` between reading the head and removing it

**Time spent**: 45 minutes

---

## Your Development Log

### Entry 1 - [11 November]
What I did was set my student ID, fork the repository, and examine the original starter code.

Specifics:

I updated my student ID (445050134) in SchedulerSimulationSync.java after cloning the repository.

The starter code was executed and the concurrency failures (IllegalThreadStateException and WATCHDOG timeout) were noted.

The broken output was saved for use in technical analysis.

Problems: Because of an unprotected critical section, several CPU threads were simultaneously picking up the same process from the ready queue.

Solution: Found that there is no mutual exclusion in the ReadyQueue methods (poll, add, snapshot, and processOf).

Two hours were spent.

### Entry 2 - [11 November]
What I carried out: Feature 1 (Using a Mutex Lock to Protect the Ready Queue) was put into practice.

Specifics:

Java.util.concurrent.locks was imported.ReentrantLock.

In the ReadyQueue class, a ReentrantLock queueLock was declared.

Lock.lock() and try/finally { lock.unlock(); } blocks were used to encapsulate all queue modification and access methods (add, poll, processOf, snapshot).

Challenges: Ensuring that the finally unlock block was not circumvented by the return statements in poll() and processOf().

The solution was to keep unlock() inside finally while safely placing the return statements inside the try block.

Two hours were spent.

### Entry 3 - [12 November]
What I did was put Feature 2 (Protecting Shared Statistics with Mutex Locks) into practice.

Specifics:

The SharedStats class now has a dedicated ReentrantLock statsLock.

All three getter methods and all three update methods (incrementContextSwitch, incrementCompletedProcess, and addServiceTime) were protected.

Because independent counters can share a lightweight mutex without experiencing performance degradation at this simulation scale, it is justified to use a single lock for statistics.

Difficulties: Avoiding lost updates during read-modify-write sequences due to RaceWindow.pause().

Solution: Made sure that the lock strictly limits each and every read and write operation on shared statistics.

Two hours were spent.

### Entry 4 - [12 November]
What I carried out: Feature 3 (Counting Semaphore and Clean Shutdown in Place of Busy Waiting) was implemented.

Specifics:

Java.util.concurrent.Semaphore was imported.

In ReadyQueue, a counting semaphore with an initial value of 0 was added.

called semaphore.acquire() in poll() and semaphore.release() in add().

The thread was removed.CpuWorker.run()'s busy-waiting loop, sleep(20).

In order to avoid deadlocks and watchdog timeouts, wakeupAllCPUs() was implemented to release blocked CPUs when all processes are finished.

Problems: CPUs were waiting on acquire(), which caused them to block indefinitely after the last process finished.

Solution: Added a check to call semaphore.release (SharedStats.totalCPUs) when the last process completes (SharedStats.getCompletedProcessCount() == SharedStats.totalProcesses).

Two hours and thirty minutes were spent.

### Entry 5 - [14 November]
What I carried out: completed the MY_WORK documentation, carried out final testing, and confirmed the output verification block.MD.
Details: Run SchedulerSimulationSync.java five times in a row to make sure that Busy-waiting polls stayed strictly at zero and that all verification checks passed with green checkmarks ($\checkmark$).double-checked that there were no changes made to the RaceWindow, Config, and verification block code.finished the MY_WORK Development Log, Reflection, and Technical Answers.MD.The two to three minute video demonstration of the code walkthrough and IDE execution was prepared and recorded.Challenges: Making sure that every verification criterion is consistently met over several runs without any watchdog timeouts or deadlocks.Solution: Confirmed that worker thread termination was handled smoothly by the counting semaphore and shutdown release mechanism.
One hour and thirty minutes were spent.

### Entry 6 - [Optional - Date and Time]
**What I did**:

**Details**:

**Challenges**:

**Solution**:

**Time spent**:

---

## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.

**Total time spent on assignment**: [X hours]

**Most challenging part**:

**Most interesting learning**:

**What I would do differently next time**:

---

# Part B: Reflection (0.5 mark)

> 🛑 **STOP:** Do **not** start this part until you have read the `README.md`, read the **entire** `SchedulerSimulationSync.java`, run it, and finished the three features.
>
> ⚠️ **WARNING:** Each answer must be **5 to 7 sentences**, in **your own words**. Copied or AI-generated answers without understanding get **0 marks for the whole assignment**. You may be asked to explain them in person.
>
> 💡 **TIP:** Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.
>
> 💡 **TIP:** Draft your answer in a few bullet points first, then turn them into sentences.

Question 1: What did you learn about synchronization from this assignment?
Through this assignment, I gained a deep, practical understanding of how concurrent threads interact with shared resources and why race conditions occur. I learned that operations like count++ are not atomic; they consist of separate read, modify, and write steps that can interleave when multiple threads execute concurrently, leading to lost updates. By implementing ReentrantLock with try/finally blocks, I realized the absolute necessity of mutual exclusion to protect critical sections safely, ensuring that even if exceptions occur, locks are always released to prevent system freezes. Furthermore, working with semaphores taught me how synchronization tools can replace inefficient busy-waiting loops with blocking mechanisms, allowing threads to sleep and wake up deterministically when resources become available.

Question 2: What was the most challenging part of this assignment and why?
The most challenging part of this assignment was designing the clean shutdown mechanism for Feature 3. When replacing the busy-waiting loop with semaphore.acquire(), the CPU threads correctly blocked when the ready queue was empty. However, once all 13 processes completed their execution, the CPU threads remained blocked on the semaphore waiting for new processes, causing the simulation to hang and trigger the watchdog timer. Figuring out how to safely wake up all sleeping CPU threads at the exact moment the final process finished required a thorough understanding of semaphore permits and thread lifecycles. I had to implement a wakeupAllCPUs() method that releases a number of permits equal to totalCPUs to ensure every waiting worker thread unblocks and terminates cleanly.

Question 3: How did you overcome the challenges you faced?
I overcame the challenges by breaking down the assignment into incremental, testable steps and utilizing systematic debugging techniques. When the watchdog kept triggering in Feature 3, I reviewed Chapter 5 of the textbook regarding producer-consumer synchronization and semaphore mechanics. I added strategic print statements to track the state of the ready queue and the semaphore permit count. By running the simulation repeatedly after each minor adjustment—and verifying that all four lines in the verification block showed green checkmarks (✔)—I could isolate whether the issue stemmed from the queue lock, the statistics counters, or the semaphore shutdown logic. Consulting the course slides and documentation also clarified the proper usage of finally blocks and semaphore releases.

Question 4: Where can the synchronization concepts be applied in real-world applications?
The synchronization concepts learned in this assignment are directly applicable to many real-world software systems, such as web servers, database management systems, and multithreaded desktop applications. For instance, in a multithreaded web server handling thousands of client requests concurrently, worker threads pull tasks from a shared request queue using mutex locks and semaphores, exactly like our ReadyQueue and CpuWorker classes. Another real-world example is an online ticketing or seat-booking system, where multiple users try to book the same seat simultaneously; mutual exclusion ensures that race conditions do not result in double-booking. Understanding critical sections, mutexes, and avoiding deadlocks is crucial for building reliable, high-performance concurrent software.

Part C: Technical Answers

# Part C: Technical Answers (0.5 mark)

> 🛑 **STOP:** You cannot answer these questions without understanding the code. Re-read `SchedulerSimulationSync.java` and **run it** first. Your answers must reference **your own code and your own output** (your student ID makes your output and your expected values unique).
>
> ⚠️ **WARNING:** Each answer must be **3 to 5 sentences**, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.
>
> 💡 **TIP:** Keep the output of the **original starter** and the output of your **final version** in text files or screenshots, so you can copy real snippets for Question 1.

## Question 1: Race Condition in Your Own Output

**Question**: Run the **original starter** (before any fix) and paste the **verification block** of that run. Which value was wrong (expected vs observed)? Explain **step by step**, with two named threads/CPUs, how **one lost update** happens on one of the shared variables (read, `RaceWindow.pause()`, write). Why can the same bug happen on a real machine even without `RaceWindow`, and why is it hard to detect?

> ⚠️ **WARNING:** The snippet must come from **your own run** (with your student ID), not from a classmate or from this README.
>
> 💡 **TIP:** Use a small timeline: *CPU-1 reads `contextSwitchCount` = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost.* If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

**Your Answer:** *(3-5 sentences)*

═══ VERIFICATION (expected values are computed from YOUR seed) ═══
  Context switches (quanta executed)     expected 27       observed 25       ✘ MISMATCH
  Completed processes                    expected 13       observed 12       ✘ MISMATCH
  Total service time (ms)                expected 59596    observed 55838    ✘ MISMATCH
  Busy-waiting polls (must be 0)         expected 0        observed 742      ✘ MISMATCH
  ✘ At least one check failed (see the ✘ lines above): a race condition or busy waiting is still present.

Explanation of the timeline: In the original starter, updating shared counters like contextSwitchCount is unprotected. Suppose contextSwitchCount is currently 10. CPU-1 reads 10, then RaceWindow.pause() preempts it. Meanwhile, CPU-2 also reads 10. CPU-1 computes 10 + 1 = 11 and writes 11. Then CPU-2 computes 10 + 1 = 11 and overwrites it with 11. Two context switches occurred, but the counter only increased by one; thus, an update was permanently lost. This bug happens on real machines due to hardware-level interleaving of machine instructions when multiple cores access memory simultaneously, and it is notoriously hard to detect because it occurs nondeterministically depending on CPU scheduling.

## Question 2: Critical Sections and Lock Granularity
Critical sections and locks: We protected the ready queue (list and map in ReadyQueue) using queueLock, and the shared statistics (contextSwitchCount, completedProcessCount, totalServiceTime in SharedStats) using statsLock.

Lock granularity choice: We used separate locks (queueLock and statsLock) rather than a single global lock. This is because the ready queue operations and the statistics updates are completely independent tasks; locking them separately increases concurrency and avoids unnecessary bottlenecks.

Mutual exclusion, progress, and bounded waiting: Mutual exclusion is strictly guaranteed because ReentrantLock allows only one thread inside a critical section at a time. However, default ReentrantLock instances are non-fair, meaning threads acquire the lock in barging order rather than strict FIFO order, which can theoretically lead to thread starvation if a thread is repeatedly beaten by incoming threads.
## Question 3: Busy Waiting vs Semaphore

Busy waiting cost: In the starter code, idle CPUs repeatedly polled the empty queue inside a while loop, resulting in 742 unnecessary Busy-waiting polls that wasted CPU processing cycles.

Semaphore value & shutdown: The semaphore tracks the number of available processes in the ready queue. Its initial value is 0 because no processes are ready before initialization (or it counts up as processes are added). Right after the numProcesses initial add() calls in main, the semaphore value equals numProcesses (e.g., 13). The last completing CPU calls release(totalCPUs) to wake up any worker threads sleeping on semaphore.acquire(), allowing them to observe the completion condition and terminate cleanly without hanging.

## Question 4: Classical Problems and Deadlock
Classical problem and roles: This scenario models the classical Producer-Consumer Problem (or bounded-buffer problem). The main thread and re-enqueuing CPUs act as producers (adding processes to the queue), while the CpuWorker threads act as consumers (taking processes from the queue).

Semaphores for a bounded queue: If the queue had a fixed capacity K, we would need three semaphores: mutex (initialized to 1 for mutual exclusion), empty (initialized to K counting empty slots), and full (initialized to 0 counting filled slots).

Deadlock scenario: A deadlock would occur if a consumer thread acquired the mutex lock before waiting on the full semaphore when the queue was empty. Since the queue is empty, the consumer blocks while holding the mutex, meaning no producer can ever access the queue to add a process, resulting in a permanent deadlock. To prevent this, we break the Hold and Wait condition by ensuring threads release mutexes before blocking on resource semaphores, or by acquiring resource semaphores outside the critical section lock.

## Summary

**Key concepts I understood through these questions:**
1.
2.
3.

**Concepts I need to study more:**
1.
2.

---

# ✅ Final Checklist (complete before submitting)

> ⚠️ **WARNING:** Go through every line. Blackboard does not accept submissions after the deadline, which is **November 14, 2026**.

**Repository**
- [ ] Repository is **PUBLIC** (Settings → Danger Zone → Visibility)
- [ ] Repository is renamed to `OS-Assignment3-YourFirstName-YourLastName`
- [ ] GitHub account uses the university email (`@std.psau.edu.sa`)

**Code**
- [ ] Student ID is set in `SchedulerSimulationSync.java` (line 304)
- [ ] My code is based **only** on the starter of this repository (nothing copied from previous assignments)
- [ ] Code compiles and runs with no errors, and terminates by itself (no `⛔ WATCHDOG`)
- [ ] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [ ] **The four verification lines are ✔ in 5 consecutive runs**
- [ ] Every lock is released in a `finally` block
- [ ] `RaceWindow`, `Config`, the verification block and the watchdog are **unchanged**
- [ ] Each feature has clear comments

**Commits**
- [ ] **At least 4 meaningful commits, ideally 7 or more**
- [ ] **One commit per feature**
- [ ] Commits are spread over **different dates** (not all in the last hour)
- [ ] Everything is **pushed** to GitHub

**This file (`MY_WORK.md`)**
- [ ] Full name and student ID filled in at the top
- [ ] Development log has **5+ entries** on different dates
- [ ] Reflection: 4 questions, 5-7 sentences each
- [ ] Technical answers: 4 questions, 3-5 sentences each, with examples from **your** output (starter output **and** final output pasted in Question 1)
- [ ] No `[...]` placeholders left
- [ ] No section headers deleted

**Video**
- [ ] 2-3 minutes long, named `StudentID_Assignment3_Demo.mp4`
- [ ] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [ ] Link is **public** (tested in an incognito window) and pasted in the **Video Link** section above

**Blackboard**
- [ ] Submit **only** the link to your public GitHub repository

> 🎯 **Good luck!** Start early, commit regularly, and make sure you can explain every line you submit.
