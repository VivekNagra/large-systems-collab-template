# Large Systems – Version Control & Team Collaboration Template

This repository is a reusable **GitHub template** intended to demonstrate modern collaboration practices:
Issues + Project board, small Pull Requests, reviews, CODEOWNERS, automation (labels and board movement), and a consistent developer environment via Dev Containers.

It is designed to be reused as a starting point for future team projects.

## Table of Contents
1. About the Project
2. Branching Strategy decision
3. Getting Started (how to clone it)
4. Automation & Workflows
5. Metrics
6. License

---

## 1. About the Project

**Purpose:** Demonstrate disciplined collaboration workflows on GitHub with a repository that is configured as a reusable template.

**What is included in this repo**
- Minimal runnable .NET 8 Web API (small codebase on purpose)
- Dev Container configuration for consistent environments
- Collaboration documentation (README + CONTRIBUTING)
- (Added in later sections) Issue/PR templates, CODEOWNERS, workflows (labeler + metrics), and Project automation

---

## 2. Branching Strategy decision

We use **GitHub Flow**:

- `main` is always in a working state
- Work is done in **short-lived branches** created from `main`
- Each task is tracked as a GitHub Issue and implemented via a Pull Request
- PRs are small, focused, and linked to an Issue (e.g., `Fixes #12`)
- When ready, PRs are reviewed and merged into `main`

**Branch naming convention**
- `feature/<short-description>` (new functionality)
- `bugfix/<short-description>` (bug fixes)
- `docs/<short-description>` (documentation-only changes)
- `chore/<short-description>` (maintenance / tooling)

**Why GitHub Flow**
It is simple, easy to enforce with branch protection rules, and fits well with Issue-driven development and Pull Request reviews.

---

## 3. Getting Started (how to clone it)

### Clone the repository
```bash
git clone <YOUR_REPO_URL>
cd <YOUR_REPO_FOLDER>
```
## Run locally (without Dev Container)

Requirements:

- .NET SDK 8.x

## Run:
```bash
dotnet restore
dotnet run --project src/MyTemplate.Api/MyTemplate.Api.csproj
```

The API should be available at:
http://localhost:5080 

Test endpoint:
GET http://localhost:5080/health

---

## 4. Automation & Workflows
This repo is configured to support automation that improves collaboration and reduces manual work:
Planned / configured automation (added in later sections):
- Issue movement on Project board
    - When a PR is opened → Issue moves to In Progress
    - When PR is merged/closed → Issue moves to Done
- Label automation
    - A GitHub Actions labeler applies labels based on changed paths (e.g., /docs/** → documentation)

- Metrics workflow
    - A scheduled workflow produces basic collaboration metrics (PR volume / lead time signals)

--- 

## 5. Metrics
We track lightweight collaboration metrics to reflect on developer efficiency and team workflow:
- Time from Issue creation → PR merged
- Number of PRs merged per week
- Metrics table with sample Issues and PRs
- A scheduled workflow that outputs a weekly summary in GitHub Actions logs

---

## 6. License
This repository is licensed under the MIT License. See LICENSE.


## Using this repository as a template
Once the repository is configured as a Template Repository (GitHub Settings → “Template repository”), you can reuse it by:

- Click Use this template

- Create a new repository under your account/team

- Update:
    - Repository name and description
    - CODEOWNERS 
    - Project board reuse or create a new one per project