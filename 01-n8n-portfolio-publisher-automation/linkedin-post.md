Built a real automation system using n8n.

Project: n8n Portfolio Publisher Automation

Problem:
Managing portfolio projects manually can become repetitive and inconsistent. Every new automation project needs a README, setup guide, workflow summary, LinkedIn post draft, and workflow export. Doing this manually takes time and often leads to incomplete documentation. This workflow solves that by automatically generating structured portfolio files and pushing them into GitHub.

Solution:
Designed an end-to-end workflow that captures input via form, processes data using automation logic, and publishes structured outputs directly to GitHub.

Tech Stack:
n8n, GitHub API, JavaScript, Markdown, Workflow JSON

Workflow:
n8n Form collects project details → Code node processes the input → Documentation files are generated dynamically → GitHub nodes create project files in the repository → Workflow JSON is added for import and reuse → LinkedIn post draft is generated for public sharing.

What I learned:
I learned how to design a reusable automation pipeline that accepts structured input, transforms it into multiple documentation assets, and publishes those files to GitHub automatically. This project helped me understand n8n triggers, form inputs, Code node logic, GitHub API integration, dynamic expressions, and portfolio-focused automation design.

This project is part of my journey building practical automation systems instead of just learning tools.

All outputs including documentation and workflow JSON are generated automatically.

#n8n #Automation #WorkflowAutomation #GitHub #Projects #DataEngineering
