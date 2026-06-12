# CS351 — Course Repository
**Student:** Huang Yen-Chun (Cyan) · GitHub: [Cyanlit](https://github.com/Cyanlit)
**Course:** CS351 — AI-Assisted Software Development · Yuan Ze University

---

## Table of Contents
1. [Personal Website](#1-personal-website)
2. [Course Deliverables and Learning Log](#2-course-deliverables-and-learning-log)
3. [Project 0 — Two Sum](#3-project-0--two-sum)
4. [Project B — CSV Mini Database and Query Engine](#4-project-b--csv-mini-database-and-query-engine)
5. [GitHub Workflow Evidence](#5-github-workflow-evidence)
6. [Reflections on AI-Assisted Development](#6-reflections-on-ai-assisted-development)
---
## Quick Links

| Item | Link |
|------|------|
| Course repository (this repo) | https://github.com/Cyanlit/11402_CS351 |
| Personal website | https://cyanlit.github.io/ |
| Personal website source | https://github.com/Cyanlit/Cyanlit.github.io |
| Project 0 (Two Sum) | https://github.com/Cyanlit/11402_CS351_Project0 |
| Project B (CSV query engine) | https://github.com/Cyanlit/11402_CS351_ProjectB |
| Official course reference | https://github.com/yfhuang/YZUCSE_CS351 |

## 1. Personal Website

**URL:** https://cyanlit.github.io/
**Repo:** https://github.com/Cyanlit/Cyanlit.github.io

### Tech Stack
| Layer | Choice |
|-------|--------|
| Markup | HTML5 (single page, semantic structure) |
| Styling | Inline / lightweight CSS — clean, minimal, text-focused layout |
| Hosting | GitHub Pages (free static site hosting via `Cyanlit.github.io`) |
| Assets | Personal profile photo, plus README content presented as a personal bio for the page body |

### Design Philosophy
- **Minimalist academic-style profile** — the overall presentation is closer to a personal résumé / research statement page than a flashy portfolio, reflecting a focus on CS fundamentals over visual polish
- **Content-first layout** — sections proceed in order: introduction → areas of interest → technical background → personal philosophy, similar to a faculty or graduate student homepage structure
- **Single profile photo with text blocks** — avoids heavy graphics or animation, keeping the page lightweight and readable on any device
- **Links back to GitHub profile** — connects the static site to the actual GitHub account
### Content Highlights
- **About Me** — introduces the author as a senior computer science student focused on data structures, algorithms, operating systems, computer organization, and software development, with interest in both low-level implementation details and overall system architecture
- **Areas of Interest** — data structures and algorithms, systems programming, backend development
- **Technical Background** — programming languages: C++, Python, TypeScript; systems: Git/version control, basic networking concepts
- **Philosophy** — emphasizes that solid fundamentals are the basis for long-term growth, built through disciplined and consistent practice
### Personal Thoughts and Future Improvements
- The site content is currently fairly text-heavy; a future version could add a **project showcase section** linking to Project 0 / Project B, with CI badges and sample test results
- Add a **dark/light theme toggle** to improve comfort across different viewing environments
- Add a **dynamic timeline / recent activity section** summarizing recent course progress and commit history, so visitors can see ongoing progress rather than just a static snapshot
- Add a small **CSS grid layout** for the technical background section, so it can scale better as the skills list grows
---

## 2. Course Deliverables and Learning Log

### What I Completed
| Deliverable | Description | Link |
|-------------|-------------|------|
| Project 0 | Two Sum — two algorithmic approaches (O(n²) and O(n)), full test suite, CI/CD, and Docker containerization | [→ Repo](https://github.com/Cyanlit/11402_CS351_Project0) |
| Project B | CSV mini database and query engine — load, index, and query CSV data via CLI | [→ Repo](https://github.com/Cyanlit/11402_CS351_ProjectB) |
| Portfolio | Minimalist personal profile site deployed on GitHub Pages | [→ Site](https://cyanlit.github.io/) |

### Key Learning Milestones
- **Comparing two algorithms** — implemented both a brute-force solution and a hash-table-based solution, directly comparing the O(n²) and O(n) behavior
- **Structured project documentation** — Project 0 includes a full set of `docs/` files following software engineering conventions (intended use, planning, SRS, SDS, test plan, acceptance tests, traceability matrix, deployment guide, known issues)
- **CI/CD with GitHub Actions** — set up a workflow that automatically builds the C++ project and runs the test suite on every push and pull request
- **Containerization with Docker** — wrote a `Dockerfile` so the build and test process is reproducible in a container, independent of the host environment
- **Transparent AI usage** — Project 0 explicitly documents how AI was involved through separate `AI_POLICY.md` and `AI_USAGE.md` files
### Reflections

Before this course, my use of Git was fairly basic — mostly just pushing finished code with little structure or documentation. CS351 changed that significantly.

In Project 0 in particular, I didn't stop at just writing the algorithm. I built a full set of documents (SRS, SDS, test plan, acceptance tests, traceability matrix), trying to mirror how a real small software project handles specification and verification. This shifted how I thought about the problem — no longer just "write a function that solves Two Sum," but a small system involving requirements, design decisions, test coverage, and deployment considerations.

Working with AI tools throughout this process taught me that **the effectiveness of AI assistance is directly proportional to how clearly I can describe the problem**. When I provided precise specifications — exact function signatures, complexity requirements, specific test categories — the resulting code and documentation needed far fewer corrections; conversely, vaguely described problems required much more adjustment afterward.

---

## 3. Project 0 — Two Sum

**Repo:** https://github.com/Cyanlit/11402_CS351_Project0

### Problem Description

Given an array of integers `nums` and an integer `target`, return the indices of the two numbers that add up to `target`.

**Assumptions:**
- Each input has exactly one solution
- The same element cannot be used twice
- The order of the returned indices does not matter
**Example:**
```
Input: nums = [2, 7, 11, 15], target = 9
Output: [0, 1]
Explanation: nums[0] + nums[1] == 2 + 7 == 9
```

### Algorithm Design

Two independent solutions were required, both using `std::vector<int>` for input and output:

| Function | Approach | Time Complexity |
|----------|----------|------------------|
| `TwoSumArray` | Uses a nested double loop to check every pair of elements | O(n²) |
| `TwoSumHashTable` | Uses an STL hash table (`unordered_map`) in a single pass, recording previously seen values and their indices | O(n) |

The hash-table solution trades a small amount of extra memory for a substantial reduction in runtime, with the difference becoming more pronounced as input size grows — a concrete example of a time/space trade-off.

### Repository Structure

```
.
├── docs/                          # Complete software documentation set
│   ├── 00_intended_use.md        # Problem definition and scope
│   ├── 01_plan.md                # Project plan
│   ├── 02_SRS.md                 # Software requirements specification
│   ├── 03_SDS.md                 # Software design specification
│   ├── 04_test_plan.md           # Test strategy
│   ├── 05_acceptance_tests.md    # Acceptance criteria
│   ├── 06_traceability.md        # Requirements traceability matrix
│   ├── 07_deploy.md              # Deployment guide
│   └── 08_known_issues.md        # Known limitations
├── src/                           # Source code (TwoSumArray, TwoSumHashTable)
├── include/                       # Header files
├── test/                          # Test files
├── .github/workflows/             # GitHub Actions CI configuration
├── Dockerfile                     # Container build definition
├── CHANGELOG.md                   # Version history
├── AI_POLICY.md                   # AI usage policy for this project
├── AI_USAGE.md                    # Documentation of AI-generated content
└── README.md                      # Project overview
```

### Development Process

1. **Define scope first** — before writing any code, drafted `00_intended_use.md` and `01_plan.md` together with AI to clarify exactly what "Two Sum" meant for this assignment (input format, output format, edge cases to support)
2. **Write SRS and SDS** — turned the informal problem description into formal requirements (`02_SRS.md`) and a design document covering both the array-based and hash-table approaches (`03_SDS.md`)
3. **Implement both solutions** — `TwoSumArray` (O(n²)) and `TwoSumHashTable` (O(n)), both accepting `std::vector<int>` and a target value, returning indices as `std::vector<int>`
4. **Build the test suite** — following `04_test_plan.md` and `05_acceptance_tests.md`, covering basic examples, negative numbers, duplicates, answers containing zero, and minimal/small input sizes
5. **Set up CI/CD** — wrote a GitHub Actions workflow (`.github/workflows/`) triggered on every `push` and `pull_request`, building the project and running the full test suite
6. **Containerize the build** — wrote a `Dockerfile` so the project can be built and tested via:
   ```bash
   docker build -t twosum .
   docker run twosum
   ```
7. **Document AI involvement** — maintained `AI_POLICY.md` (how AI was used and its limitations in this project) and `AI_USAGE.md` (recording which content was actually AI-generated versus written independently)
### Local Build

```bash
# Clone the repository
git clone https://github.com/Cyanlit/11402_CS351_Project0.git
cd 11402_CS351_Project0

# Build the project
cd src
g++ -std=c++17 -o twosum main.cpp twosum.cpp

# Run tests
./twosum
```

### Development History

- **27 commits total**, roughly following: skeleton setup → core algorithm implementation → test suite → CI/CD configuration → Docker containerization → documentation
- All integration done on the **`main`** branch
- The `docs/` folder was built incrementally alongside development, not written after the fact
### Test Results

- The test suite covers: standard examples, negative inputs, duplicate values, cases where the answer includes zero, and minimal-size arrays
- All tests run automatically via GitHub Actions on every push and pull request:
```
push / pull_request
      │
      ▼
  build (g++ / CMake)
      │
      ▼
  run test suite
      │
   ✅ pass → CI green
   ❌ fail → CI red
```

### Project Status

- ✅ Core algorithms complete (`TwoSumArray`, `TwoSumHashTable`)
- ✅ Full test suite covering edge cases
- ✅ GitHub Actions CI/CD
- ✅ Docker containerization
- ✅ Complete software documentation set (SRS, SDS, test plan, traceability matrix, deployment, known issues)
### Project Highlights

The most valuable part of this project isn't the algorithm itself — Two Sum is a well-known problem — but **the complete documentation process built around it**. At first, writing an SRS and SDS for such a small problem felt like overkill, but the process forced me to make explicit decisions I would normally make intuitively, such as "what actually counts as an edge case?" and "how do I demonstrate that requirements are actually covered by tests?" (i.e., the traceability matrix). AI was helpful for quickly scaffolding the structure of each document, but the actual technical content — especially the mapping between requirements, design, and tests — still had to be filled in and verified by me.

---

## 4. Project B — CSV Mini Database and Query Engine

**Repo:** https://github.com/Cyanlit/11402_CS351_ProjectB

### Project Goal

Build a lightweight database system on top of CSV files — after loading a CSV file, allow the user to perform query-like operations on the data (filtering, sorting, basic CRUD), conceptually similar to a very small SQL engine.

### Key Features

- **CSV file handling** — load, parse, and manage CSV files
- **Query engine** — execute filtering, sorting, and row manipulation queries
- **Command-line interface** — simple commands for loading files and running queries
- **Performance considerations** — designed with efficiency in mind for data processing and retrieval
### Data Design

- Input data is read directly from CSV files, with each row treated as a record and each column as a field
- The query engine operates on these records, supporting filter-based queries (e.g., selecting rows matching a condition) as well as basic sorting/manipulation
- The choice of Pandas for data handling and SQLite as the storage backend reflects the "mini database" design philosophy — quickly converting CSV data into a structured, queryable form rather than implementing a storage engine from scratch
### Usage

```bash
# Install dependencies
pip install -r requirements.txt

# Run the application
python main.py

# Example commands within the application
load <filename>
query <your_query>
```

### Development Process

1. **Establish project goals first** — wrote a project overview and feature list (CSV handling, query engine, CLI, performance) before implementation, so scope was clear from the start
2. **Choose the tech stack** — used Python as the implementation language, with Pandas for data handling and SQLite as the storage backend, balancing the learning value of building from scratch against using practical tools
3. **Implement the core flow** — `load <filename>` loads a CSV into memory/database, `query <your_query>` performs filter/sort operations on it
4. **Iterative collaboration with AI** — described the overall architecture (CSV loading → storage layer → query engine → CLI), had AI help scaffold initial versions of each part, then manually tested the CLI with real sample CSV files to confirm the output matched expectations
### Development History

- **4 commits total**, covering: initial project setup and README, core CSV loading logic, query engine implementation, and CLI integration
- This smaller-scale project was developed directly on the **`main`** branch
### Project Highlights

This project provides a good contrast to Project 0. Project 0 focused on a single, well-defined algorithm with extensive documentation; Project B focused on **integrating multiple components into a working tool** — file I/O, the storage layer, the query parser, and the CLI all had to work correctly together. The biggest takeaway: each component "looking fine" individually wasn't enough; I had to actually run `load` followed by `query` against real sample CSV files to catch integration issues that wouldn't be visible just from reading the code.

---

## 5. GitHub Workflow Evidence

### Commit History
- **Project 0:** 27 commits — reflecting the full progression from skeleton setup, implementation, testing, CI, Docker, to documentation
- **Project B:** 12 commits — roughly one per major development phase (setup, CSV handling, query engine, CLI)
- **Personal website:** 11 commits — multiple iterations on content and layout
### Branches
- All three repositories currently use **`main`** as the primary branch
- Project 0's higher commit count and dedicated `docs/` folder reflect that it was the more heavily engineered deliverable in this course; Project B had fewer commits, partly due to experience gained from Project 0 and the use of feature branches
- In the future, splitting major changes into feature branches with pull requests could more clearly demonstrate a code review process
### CI/CD (Project 0)

The GitHub Actions workflow under `.github/workflows/` triggers on every push and pull request:

```
push / pull_request
      │
      ▼
  build C++ project (g++ / CMake)
      │
      ▼
  run full test suite
      │
   ✅ pass → build marked successful
   ❌ fail → build marked failed
```

### Containerization (Project 0)

The project includes a `Dockerfile`, making the build and test environment reproducible:

```bash
docker build -t twosum .
docker run twosum
```

This means the CI environment, a grader's machine, and my own machine should, in theory, all produce the same build and test results.

---

## 6. Reflections on AI-Assisted Development

The main AI tool I used in this course was an AI coding assistant integrated into the editor, used across all three deliverables (personal website, Project 0, Project B).

### How I Interacted with AI

Rather than treating AI as a one-shot code generator, I incorporated it into an iterative loop:

```
Me  →  describe the goal, constraints, and expected output
AI  →  produce a draft of code, documentation, or configuration
Me  →  build/run, check results against the spec
Me  →  "this test case is missing" / "this part of the SRS needs revision" / "the Dockerfile needs adjusting"
AI  →  update the corresponding files
Me  →  re-test, then commit once verified
```

This loop repeated for every component — algorithm implementations, each document, the CI workflow, and the Dockerfile.

### Example 1 — Project 0's Documentation Set

Instead of asking "give me a README," I had AI produce each document in the `docs/` folder separately — first the intended use definition, then SRS, SDS, test plan, and so on. Going one document at a time, with each previous document as context for the next, produced documents that were far more consistent and traceable than requesting the whole set at once. I then reviewed each document individually and corrected the technical details myself (e.g., exact complexity statements, exact test case descriptions).

### Example 2 — Project 0's Algorithms

For `TwoSumArray` and `TwoSumHashTable`, I explicitly specified the function signatures (`std::vector<int>` input/output) and required complexity (O(n²) and O(n) respectively), and had AI implement both versions. I then asked: *"What edge cases should the test suite for these implementations cover?"* — AI listed cases like duplicate values and answers containing zero that I hadn't specifically considered; after confirming these were reasonable, I had AI write the corresponding test code.

### Example 3 — Project B

For Project B, I described the entire flow — CSV loading, the query engine, and the CLI — using the actual commands a user would type (`load <filename>`, `query <your_query>`). AI produced an initial implementation of the relevant files in one pass. Since this project had much less upfront documentation than Project 0, I relied more heavily on **manual testing with sample CSV files** to verify correctness — actually running `load` and `query` commands and checking that the output matched expectations.

### What I Did Myself

- **Determined scope and structure** — decided what each document in Project 0's `docs/` folder should contain, and how to define the minimal feature set for Project B
- **Verified complexity claims** — confirmed that the actual behavior of `TwoSumArray` and `TwoSumHashTable` truly matched the documented O(n²) and O(n) claims
- **Ran and reviewed test results** — confirmed the test suite passed both locally and in CI, rather than trusting AI-generated tests just because they "looked reasonable"
- **Final review before each commit** — every piece of code and documentation in each commit was something I personally read and understood
### What I Learned

1. **Documentation can be written iteratively, just like code.** Working on one document at a time, building on the context of the previous one, produced more coherent `docs/` content than requesting the entire set at once.
2. **Complexity and correctness claims need independent verification.** AI-implemented algorithms may "look like" they meet the claimed complexity, but confirming whether that's actually true — and whether tests genuinely cover the relevant cases — is my own responsibility.
3. **Smaller, well-scoped projects (like Project B) shift the burden of verification onto manual testing.** Without a full documentation/test plan structure, hands-on testing with real input files was my primary way of catching integration issues.
