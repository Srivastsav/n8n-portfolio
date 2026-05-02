# 01 - AI Portfolio Publisher & Website Updater v2

## Overview

This project automates the end-to-end process of publishing new portfolio projects, from generating documentation and social media posts using AI to updating the portfolio website and creating a GitHub pull request.

## Business Problem

Manual portfolio updates are time-consuming, repetitive, and prone to inconsistencies, involving documentation, GitHub uploads, website edits, and pull request creation.

## Solution

An n8n workflow automates the entire portfolio publishing process, from content generation using Google Gemini to GitHub repository updates and website card integration, significantly reducing manual effort.

## Technical Architecture

The solution leverages n8n for orchestration, Google Gemini API for AI content generation, and GitHub API for repository and website updates, all powered by JavaScript, HTML, and Markdown.

## Tools Used

n8n, Google Gemini API, GitHub API, JavaScript, HTML, Markdown

## Workflow Steps

1. Form submission captures structured project details.
2. A Code node prepares a controlled Gemini API request.
3. Gemini generates portfolio-ready content in structured JSON.
4. A parser extracts the AI output and keeps the original form data.
5. n8n generates README.md, setup-guide.md, workflow-summary.md, linkedin-post.md, and workflow.json files.
6. The project files are uploaded to the n8n portfolio GitHub repository.
7. The workflow retrieves the portfolio website index.html file from GitHub and decodes the base64 content.
8. A website project card is generated using AI-supported content.
9. The card is inserted or updated in the System Case Files section using project-specific HTML markers.
10. A new GitHub branch is created.
11. The updated index.html file is committed through the GitHub API.
12. A pull request is created so the website update can be reviewed and merged manually.

## Business Impact

This automation reduces manual portfolio publishing effort, standardizes project documentation, prevents duplicate website cards, and introduces a reviewable GitHub pull request process for portfolio website updates. The pattern is adaptable for internal knowledge bases, automation catalogs, release notes, SOP libraries, and technical documentation portals.

## Failure Handling

The workflow includes error handling for API calls and file operations. The pull request mechanism ensures that any website update issues can be reviewed and manually corrected before merging to the main branch.

## AI Layer

This workflow uses Google Gemini API as the AI content generation layer.

The Gemini step converts raw project details into structured portfolio-ready content, including:

- Business problem summary
- Solution summary
- Technical architecture explanation
- Workflow steps
- Business impact
- Failure-handling notes
- README content
- Workflow summary
- LinkedIn post
- Website card content

To control usage, the workflow uses one Gemini API call per project, a Flash model, limited output tokens, and a manual trigger.

## Files Included

- README.md
- setup-guide.md
- linkedin-post.md
- workflow-summary.md
- workflow.json

## Workflow Architecture

![Workflow Architecture](images/workflow-architecture.png)

## Project Status

Completed v2 workflow with AI content generation, GitHub publishing, portfolio website update, upsert logic, dynamic branch creation, and pull request creation.

## Date Created

2026-05-02
