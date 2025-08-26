# Task: Build an Agentic AI Workflow for NIST SP 800 Updates & Applicability Summaries

## Objective
Develop an **Agentic AI Workflow** that automatically retrieves the **latest NIST SP 800-series compliance updates**, extracts their contents, determines **applicability to IT software development firms**, summarizes the findings, and publishes results to GitHub via Pull Request. The workflow should be implemented using an agentic SDK (e.g., **OpenAI Agents SDK**, **Google Agent Development Kit**, or another suitable framework) and support deployment as a containerized service.

The workflow is expected to perform the following functions:

---

## Workflow Functions

1. **Compliance Update Retrieval**
   - Search and retrieve the **latest NIST SP 800-series updates**(e.g top 10 news items) from the internet (e.g., using a **Google MCP server** or similar search tool). 
   - The topic may be provided to the agent via a **REST API**, **CLI input**, or can be **hard-coded** for initial testing.

2. **Content Extraction**
   - Extract the full content of the news articles in **Markdown format**.

3. **Domain Applicability/Filtering**
   - From the extracted content, identify and retain only the sections that are **relevant to IT and software development organizations**.
   - Focus on content that references or implies:
     - **Secure software development** (e.g., SDLC, CI/CD, code review, SAST/DAST, supply-chain security, SBOM)
     - **Cloud-native/DevOps** practices (e.g., pipelines, containerization, IaC)
     - **Handling of CUI/PII** in software systems
     - **Mappings to NIST SP 800-53 / 800-171 / 800-218 (SSDF)** that affect software teams

4. **Summarization**
   - From the filtered content, produce a clear and concise **one-page summary in Markdown** that highlights:
     - The **latest updates** discovered (with dates/versions)
     - **What matters for IT software development firms** (plain-language takeaways)
     - **Key actions/checklists** mapped to relevant controls/practices (e.g., 800-53 family codes, 800-171 requirements, SSDF tasks)
     - **Citations** back to the sources
     - etc

4. **Publishing** - Automatically publish the summary to a **GitHub repository** by creating a **Pull Request** (e.g., using the **GitHub MCP server**).

---

## Workflow Deployment

- Support Containerization & Deployment
- For an example package the workflow into a **Docker image**.
- Ensure the solution can be easily deployed and executed within a **Docker container**.


---


## Expected Deliverables

- A fully functional workflow that meets all specified requirements.
- A **Dockerfile** along with clear deployment instructions.


---


## Code Delivery

- Provide the complete **source code** (preferably hosted on your GitHub and share the repository link with us).
- Include comprehensive **documentation** (README) with setup instructions, dependency details, and usage examples.
