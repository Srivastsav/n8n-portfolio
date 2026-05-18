# 05 - test

## Overview

This project is an AI-powered n8n workflow automation built to solve a practical portfolio publishing and website update problem.

## Business Problem

test

## Solution

Designed an end-to-end n8n workflow that captures project input, generates structured portfolio documentation, publishes files to GitHub, updates the portfolio website, and creates a pull request for review.

## Technical Architecture

The workflow uses n8n form intake, Google Gemini API, JavaScript Code nodes, GitHub API requests, website HTML update logic, dynamic branch creation, and pull request automation.

## Tools Used

test

## Workflow Steps

test

## Business Impact

test

## Failure Handling

The workflow uses project-specific HTML markers and upsert logic to update existing cards instead of creating duplicates. GitHub changes are pushed through a pull request instead of directly modifying the main branch.

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

2026-05-18
