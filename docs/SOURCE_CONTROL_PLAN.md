# AgentBazaar Source Control Plan

## Goal

Create one clean canonical source repository for AgentBazaar production development and deployment.

## Current Status

A cleaned production source snapshot has been prepared for canonical repository import.

Snapshot verification on 2026-08-10:

- 90 source files included
- runtime data excluded
- storage uploads excluded
- databases excluded
- logs excluded
- backups excluded
- env files excluded
- secret/token/credential-named files excluded
- generated caches excluded
- secret-shaped value scan found 0 findings
- core exported Python files compile successfully

The snapshot should be imported into a private canonical source repository first, or reviewed before any public code release.

## Why This Matters

Production fixes should not live only in a server checkout. A canonical repository makes future work safer for Codex, Hermes, Kimi, and other agents because they can inspect history, review diffs, test branches, and avoid overwriting each other.

## Rules

Never commit:

- raw credentials
- API keys
- `.env` files
- database files
- runtime logs
- backups
- generated caches
- private user data
- payment provider secrets
- server-only operational files

## Recommended Steps

1. Choose the canonical AgentBazaar source repository.
2. Import the prepared cleaned source snapshot.
3. Add or review `.gitignore` before the first source commit.
4. Commit source, docs, tests, scripts, and deployment templates separately from runtime state.
5. Add a deployment note explaining how production is updated.
6. Require agents to work from branches or documented handoff locks for production changes.
7. Keep public beta docs in sync with actual production behavior.

## Public Repository Scope

This public repository may remain suitable for public beta documentation and agent onboarding. If production source contains sensitive deployment details, use a private source repository for the application code and mirror only safe public docs here.