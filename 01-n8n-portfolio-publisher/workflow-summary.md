# Workflow Summary - AI Portfolio Publisher & Website Updater v2

## Project Number

01

## Folder Name

01-n8n-portfolio-publisher

## Automation Purpose

Manual portfolio updates are time-consuming, repetitive, and prone to inconsistencies, involving documentation, GitHub uploads, website edits, and pull request creation.

## Solution Summary

An n8n workflow automates the entire portfolio publishing process, from content generation using Google Gemini to GitHub repository updates and website card integration, significantly reducing manual effort.

## Technical Stack

n8n, Google Gemini API, GitHub API, JavaScript, HTML, Markdown

## Workflow Design

The n8n workflow orchestrates AI content generation via Google Gemini, file creation, GitHub repository updates, and dynamic website card insertion, culminating in a reviewable pull request for website changes.

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

## AI Usage Control

This workflow uses one Gemini API call per project. The AI response is parsed into structured JSON and reused across README generation, workflow summary creation, LinkedIn post generation, and website card creation.
