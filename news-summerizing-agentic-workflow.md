# Task: Build an Agentic Workflow for News Summarization and Publishing

## Objective
Develop an **agentic AI workflow** that automates the process of retrieving, summarizing, and publishing news content. The system should use an agentic SDK (e.g., **OpenAI Agents SDK**, **Google Agent Development Kit**, or any other available option) and be deployable as a containerized service.

## Requirements

1. **News Retrieval**
   - Allow the user to input a news topic (via REST API, CLI, or even hard-coded for now).
   - Search and retrieve the **top 10 news items** for the given topic from the internet (e.g., using the **Google MCP server** or similar).

2. **Content Extraction**
   - Extract the news articles’ content in **Markdown format**.

3. **Summarization**
   - Summarize the important aspects of the collected news into a **one-page summary**.

4. **Publishing**
   - Publish the summary automatically to a **GitHub repository** by creating a **Pull Request** (e.g., using the **GitHub MCP server**).

5. **Containerization & Deployment**
   - Containerize the workflow as a **Docker image**.
   - Ensure it can be easily deployed and run as a Docker container.

6. **Code Delivery**
   - Provide complete **source code** (preferably published on GitHub).
   - Include clear **documentation** (README) with setup instructions, dependencies, and usage examples.

## Expected Deliverables
- Functional workflow meeting the requirements.
- Dockerfile and deployment instructions.
- GitHub repository link containing the source code.
