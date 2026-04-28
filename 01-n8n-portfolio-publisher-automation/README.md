# 01 - n8n Portfolio Publisher Automation

## Overview

This project is an n8n workflow automation built to solve a practical career and portfolio problem.

## Problem Solved

Managing portfolio projects manually can become repetitive and inconsistent. Every new automation project needs a README, setup guide, workflow summary, LinkedIn post draft, and workflow export. Doing this manually takes time and often leads to incomplete documentation. This workflow solves that by automatically generating structured portfolio files and pushing them into GitHub.

## Tools Used

n8n, GitHub API, JavaScript, Markdown, Workflow JSON

## Workflow Steps

n8n Form collects project details → Code node processes the input → Documentation files are generated dynamically → GitHub nodes create project files in the repository → Workflow JSON is added for import and reuse → LinkedIn post draft is generated for public sharing.

## Key Learning

I learned how to design a reusable automation pipeline that accepts structured input, transforms it into multiple documentation assets, and publishes those files to GitHub automatically. This project helped me understand n8n triggers, form inputs, Code node logic, GitHub API integration, dynamic expressions, and portfolio-focused automation design.

## Files Included

- README.md
- setup-guide.md
- linkedin-post.md
- workflow-summary.md

## Project Status

Completed basic documentation generation workflow.

## Date Created

2026-04-28
