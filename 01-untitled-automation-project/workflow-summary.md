# Workflow Summary - Untitled Automation Project

## Project Number

01

## Folder Name

01-untitled-automation-project

## Automation Purpose



## Solution Summary

Designed an end-to-end n8n workflow that captures project input, generates structured portfolio documentation, publishes files to GitHub, updates the portfolio website, and creates a pull request for review.

## Technical Stack

n8n, Google Gemini API, GitHub API, JavaScript, Markdown, HTML

## Workflow Design

This workflow automates portfolio project publishing by generating documentation files, uploading them to GitHub, updating the live portfolio website, and creating a pull request for review.

## Workflow Steps



## Business Impact

Reduced manual portfolio publishing effort, standardized project documentation, prevented duplicate website cards, and created a reviewable GitHub publishing process.

## Failure Handling

The workflow uses project-specific HTML markers and upsert logic to update existing cards instead of creating duplicates. GitHub changes are pushed through a pull request instead of directly modifying the main branch.

## AI Usage Control

This workflow uses one Gemini API call per project. The AI response is parsed into structured JSON and reused across README generation, workflow summary creation, LinkedIn post generation, and website card creation.
