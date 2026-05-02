# Workflow Summary - AI Portfolio Publisher & Website Updater v2

## Project Number

01

## Folder Name

01-n8n-portfolio-publisher

## Automation Purpose

Manual portfolio updates are time-consuming, repetitive, and prone to inconsistencies, involving repeated documentation, GitHub uploads, website edits, and pull request creation.

## Solution Summary

An n8n-powered automation workflow that leverages Google Gemini to generate structured portfolio content from a form submission, then uses the GitHub API to create project files, update the portfolio website, and initiate a pull request for review.

## Technical Stack

n8n, Google Gemini API, GitHub API, JavaScript, HTML, Markdown

## Workflow Design

The n8n workflow orchestrates content generation via Gemini, file management on GitHub, and dynamic website updates, culminating in a reviewable pull request.

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

## AI Usage Control

This workflow uses one Gemini API call per project. The AI response is parsed into structured JSON and reused across README generation, workflow summary creation, LinkedIn post generation, and website card creation.
