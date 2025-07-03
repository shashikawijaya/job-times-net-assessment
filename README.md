# Jobs Time – Coding Exercise

---

## 📋 Problem Statement (summary)

You need to process a list of jobs based on the processing time of each job, the priority of each job, and the total time allowed. Every job is represented by a Job object, in which ProcessingTime is the time in seconds, and Priority is an integer where a lower number means a higher priority, for example:
{ ProcessingTime = 10, Priority = 3 }.

Given that each priority is unique, schedule the jobs according to the following rules:

Only one job can run at a time

Jobs with higher priorities are picked first

Jobs with a processing time greater than the remaining available time should be skipped

The maximum number of jobs that can be completed should be picked, while satisfying the rules above.

Implement the GetTotalTime method, which takes a List of jobs and the total time allowed, and returns the total processing time of the completed jobs.

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

should print 38, since jobs with priority 1, 2, 3, and 4 were executed from the given job list.

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
    public int Priority { get; set; }
}

public class JobsTime
{
    public static int GetTotalTime(List<Job> jobs, int totalAvailableTime)
    {
        throw new NotImplementedException("Waiting to be implemented.");
    }

    public static void Main(string[] args)
    {
        List<Job> jobs = new List<Job>()
        {
            new Job { ProcessingTime = 10, Priority = 3 },
            new Job { ProcessingTime = 20, Priority = 1 },
            new Job { ProcessingTime = 15, Priority = 2 },
            new Job { ProcessingTime = 22, Priority = 5 },
            new Job { ProcessingTime = 3, Priority = 4 }
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

Good luck, and have fun! 🚀
