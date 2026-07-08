# MCP GitHub App Setup

This document describes the proposed GitHub App for the ChainSolutions WealthTech organization.

## App name

WealthTech MCP Governance App

## Target organization

chainsolutions-wealthtech

## Purpose

The app coordinates repository governance through the MCP runtime.

It should help with:

- repository visibility checks;
- branch-based file proposals;
- pull request creation;
- issue tracking;
- workflow visibility;
- project coordination;
- Codespaces preparation when explicitly requested;
- public-safe audit trails.

## Initial installation scope

Start with selected repositories only.

Recommended first repository:

- chainsolutions-wealthtech/.github

Expand only after validation.

## Runtime endpoints

- https://mcp.wealthtechinnovations.com/github/webhook
- https://mcp.wealthtechinnovations.com/github/callback

## Required MCP tools

- github_status
- github_list_orgs
- github_list_repos
- github_repo_status
- github_create_branch
- github_commit_files_on_branch
- github_open_pr
- github_list_prs
- github_list_actions
- github_audit_permissions
- github_create_repository_from_template
- github_prepare_codespace

## Rules

- No direct main update.
- Use a dedicated branch.
- Open a pull request for review.
- Keep public repositories public-safe.
- Audit every MCP GitHub action.
- Create repositories from approved templates only.
- Prepare Codespaces only for explicit tasks.
