# Setup Guide - Untitled Automation Project

## Prerequisites

- n8n installed and running
- Google Gemini API key
- GitHub account
- GitHub repository for portfolio projects
- GitHub personal access token or configured GitHub credential in n8n
- Basic understanding of n8n HTTP Request and Code nodes

## Setup Steps

1. Open n8n.
2. Import or recreate the workflow.
3. Configure the form submission trigger.
4. Add project input fields such as project name, problem solved, tools used, workflow steps, and business impact.
5. Configure the Gemini API request.
6. Confirm the workflow uses one Gemini call per project.
7. Configure GitHub upload nodes for the project repository.
8. Configure GitHub API nodes for reading and updating the portfolio website.
9. Confirm the workflow creates a new branch before updating index.html.
10. Confirm the workflow creates a pull request instead of directly updating main.
11. Review the pull request and merge manually.

## Notes

This setup guide is generated automatically by the AI Portfolio Publisher workflow.
