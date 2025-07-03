# Jobs Time – Coding Exercise (C# 12, .NET 8)

Welcome!  
The purpose of this short challenge is to evaluate your ability to reason about
algorithms, write clean C# code, and communicate your solution clearly.

---

## 📋 Problem Statement (summary)

You are given a **list of jobs**.  
Each job has:

* `ProcessingTime` – the time it takes to run, in **seconds**.
* `Priority` – an **integer** where a **lower** number means **higher** priority  
  (`1` is higher priority than `2`, etc.).

You also receive a **total time budget** (in seconds).  
Your task is to _schedule the jobs_ so that – **within the available time** –
you complete as much work as possible while respecting the following rules:

1. **Only one job can run at a time.**
2. Jobs with **higher priority** are always picked first.
3. If a job’s `ProcessingTime` is **greater than the remaining time**, skip it.
4. Among all possible schedules that respect the above, pick the one that
   completes the **maximum number of jobs**.

Implement a method

```csharp
public static int GetTotalTime(List<Job> jobs, int totalAvailableTime)
```

that returns the **total processing time _actually used_** by the jobs that end
up being executed.

---

## 🧩 Example

```csharp
List<Job> jobs = new()
{
    new Job { ProcessingTime = 10, Priority = 3 },
    new Job { ProcessingTime = 20, Priority = 1 },
    new Job { ProcessingTime = 15, Priority = 2 },
    new Job { ProcessingTime = 22, Priority = 5 },
    new Job { ProcessingTime =  3, Priority = 4 }
};

Console.WriteLine(JobsTime.GetTotalTime(jobs, 40)); // ➜ 38
```

Explanation:

* The scheduler considers jobs in priority order: **1, 2, 3, 4, 5**.
* Job #1 needs `20` s → **chosen** (remaining time = 20).
* Job #2 needs `15` s → **chosen** (remaining time = 5).
* Job #3 needs `10` s → **skipped** (too long).
* Job #4 needs `3` s  → **chosen** (remaining time = 2).
* Job #5 needs `22` s → **skipped**.

Total time actually spent = `20 + 15 + 3 = 38 s`.

---

## 🚀 Starter Code

Copy the snippet below into your IDE (or fork the repo, if provided).  
Your job is to replace the `NotImplementedException` with a working
implementation.

```csharp
using System;
using System.Collections.Generic;

public class Job
{
    public int ProcessingTime { get; set; }
    public int Priority       { get; set; }
}

public class JobsTime
{
    public static int GetTotalTime(List<Job> jobs, int totalAvailableTime)
    {
        // TODO: implement
        throw new NotImplementedException("Waiting to be implemented.");
    }

    public static void Main(string[] args)
    {
        List<Job> jobs = new()
        {
            new Job { ProcessingTime = 10, Priority = 3 },
            new Job { ProcessingTime = 20, Priority = 1 },
            new Job { ProcessingTime = 15, Priority = 2 },
            new Job { ProcessingTime = 22, Priority = 5 },
            new Job { ProcessingTime =  3, Priority = 4 }
        };

        Console.WriteLine(JobsTime.GetTotalTime(jobs, 40));
    }
}
```

---

## ✅ Deliverables

* **Source code** (`.cs` file or small project) containing  
  your `GetTotalTime` implementation.
* A **README** (optional) explaining your approach, complexity analysis, and
  any trade‑offs or assumptions you made.
* (Optional but welcomed) **Unit tests** that demonstrate your solution works.

---

## 🕑 Expected Duration
This exercise should take **~30 minutes**.  
Focus on clarity, correctness, and idiomatic C# – _premature optimisation is
not required_.

---

## 🔍 Evaluation Criteria

| Weight | Aspect                               |
|-------:|--------------------------------------|
| 40 %   | Correctness & edge‑case handling     |
| 20 %   | Code readability & maintainability   |
| 20 %   | Use of appropriate data structures   |
| 10 %   | Time & space complexity awareness    |
| 10 %   | Tests / demonstration / explanation  |

Good luck, and have fun! 🚀
