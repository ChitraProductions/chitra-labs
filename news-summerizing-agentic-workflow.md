# Task: Build an Agentic Workflow for News Summarization and Publishing

## Objective

Develop an **agentic AI workflow** that automates the process of retrieving, summarizing, and publishing news content. The workflow could be built using an agentic SDK (e.g., **OpenAI Agents SDK**, **Google Agent Development Kit**, or any other suitable framework) and support deployment as a containerized service.

The workflow is expected to perform the following functions:


---


## Workflow Functions

1. **News Retrieval**
   - Search and retrieve the **top 10 news items** for a given topic from the internet (e.g., using the **Google MCP server** or a similar tool).
   - The topic may be provided to the agent via a **REST API**, **CLI input**, or can be **hard-coded** for initial testing.

2. **Content Extraction**
   - Extract the full content of the news articles in **Markdown format**.

3. **Summarization**
   - Generate a concise summary(e.g **one-page summary**) highlighting the most important aspects of the collected news.

4. **Publishing**
   - Automatically publish the summary to a **GitHub repository** by creating a **Pull Request** (e.g., using the **GitHub MCP server**).


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
