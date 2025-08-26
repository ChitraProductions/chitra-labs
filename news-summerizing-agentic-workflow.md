# Task: Build an Agentic Workflow for NIST SP 800 Updates & Applicability Summaries

## Objective
Develop an **agentic AI workflow** that automatically retrieves the **latest NIST SP 800-series compliance updates**, extracts their contents, determines **applicability to IT software development firms**, summarizes the findings, and publishes results to GitHub via Pull Request. The workflow should be implemented using an agentic SDK (e.g., **OpenAI Agents SDK**, **Google Agent Development Kit**, or another suitable framework) and support deployment as a containerized service.

The workflow is expected to perform the following functions:

---

## Workflow Functions

1. **Compliance Update Retrieval**
   - Search and retrieve the **latest NIST SP 800-series updates** from the internet (e.g., using a **Google MCP server** or similar search tool).
   - Accept input for what to fetch via **REST API**, **CLI**, or **hard-coded** values for initial testing (e.g., “SP 800-53”, “SP 800-171”, “SP 800-218 SSDF”, “recent updates”).
   - Collect at least **top 10 relevant items** (news posts, update notes, official pages, PDFs) and capture source URLs for citation.

2. **Content Extraction**
   - Extract the full text/content of each retrieved item into **Markdown format**, preserving:
     - **Title, source, publication date, version/revision**
     - **Body text** (normalized to Markdown)
     - **Citations/URLs** for traceability

3. **Domain Applicability Filtering**
   - Using the domain profile **“IT software development firms”**, filter each extracted item to keep **only the portions relevant to software development organizations**.
   - Focus on content that references or implies:
     - **Secure software development** (e.g., SDLC, CI/CD, code review, SAST/DAST, supply-chain security, SBOM)
     - **Cloud-native/DevOps** practices (e.g., pipelines, containerization, IaC)
     - **Handling of CUI/PII** in software systems
     - **Mappings to NIST SP 800-53 / 800-171 / 800-218 (SSDF)** that affect software teams
   - Output: a **filtered Markdown** file per item (e.g., `sources/<slug>-filtered.md`) that includes:
     - The **original title, source, and date**
     - The **relevant excerpts only** (remove unrelated sections)
     - Brief **inline notes** (optional) explaining why a passage is relevant to software development

4. **Summarization**
   - Generate a concise **one-page Markdown summary** highlighting:
     - The **latest updates** discovered (with dates/versions)
     - **What matters for IT software development firms** (plain-language takeaways)
     - **Key actions/checklists** mapped to relevant controls/practices (e.g., 800-53 family codes, 800-171 requirements, SSDF tasks)
     - **Citations** back to the sources

5. **Publishing**
   - Automatically create a **GitHub Pull Request** containing:
     - `sources/` folder with **per-item Markdown** extractions
     - `outputs/applicability.json`
     - `outputs/summary.md`
     - A short **PR description** summarizing changes and linking sources

---

## Workflow Deployment

- **Containerization & Execution**
  - Package the workflow into a **Docker image**.
  - Provide a simple way to run via **Docker** (e.g., `docker run …` with environment variables for API keys, repo, branch).
- **Configuration**
  - Support configuration via environment variables (e.g., search keys, GitHub token/repo/branch, topic/SP identifiers).

---

## Expected Deliverables

- A fully functional workflow that meets all specified requirements.
- A **Dockerfile** along with clear deployment instructions (build, run, configuration).
- Example output artifacts:
  - `sources/*.md` (extracted items)
  - `outputs/applicability.json` (structured applicability results)
  - `outputs/summary.md` (one-page summary with citations)

---

## Code Delivery

- Provide the complete **source code** (preferably hosted on your GitHub; share the repository link).
- Include comprehensive **documentation** (README) with:
  - Setup instructions and dependencies
  - How to run via CLI/REST and Docker
  - Example inputs/commands and expected outputs
  - Notes on agentic SDKs/MCP servers used (e.g., Google search MCP, GitHub MCP)

