# 01 - AI Portfolio Publisher & Website Updater v2

## Overview

This project automates the entire portfolio publishing process, from content generation to website updates and GitHub pull requests, using n8n and AI.

## Business Problem

Manual portfolio updates are time-consuming, repetitive, and prone to inconsistencies, involving repeated documentation, GitHub uploads, website edits, and pull request creation.

## Solution

An n8n-powered automation workflow that leverages Google Gemini to generate structured portfolio content from a form submission, then uses the GitHub API to create project files, update the portfolio website, and initiate a pull request for review.

## Technical Architecture

The solution uses n8n as the orchestration engine. Google Gemini API generates diverse content formats. The GitHub API handles file creation, updates, and pull request management. JavaScript and HTML are used for website manipulation, and Markdown for documentation.

## Tools Used

n8n, Google Gemini API, GitHub API, JavaScript, HTML, Markdown

## Workflow Steps

1. Form submission captures project details.
2. Gemini generates structured portfolio content.
3. n8n creates README, setup guide, workflow summary, LinkedIn post, and workflow JSON files.
4. Project files are uploaded to the GitHub portfolio repository.
5. The portfolio website index.html file is retrieved and decoded.
6. A project card is generated and inserted or updated using marker-based upsert logic.
7. A new GitHub branch is created.
8. The website update is committed through the GitHub API.
9. A pull request is created for manual review and merge.

## Business Impact

Significantly reduced manual effort in portfolio publishing, ensured standardized project documentation, prevented duplicate website cards, and introduced a robust, reviewable GitHub pull request process for website updates.

## Failure Handling

The n8n workflow includes error handling for API calls and file operations. GitHub pull requests provide a safety net for website updates, allowing manual review and rollback if issues arise.

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
