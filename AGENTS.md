# AGENTS

## Purpose

This repository contains concepts, templates and architecture documents.

It does not contain implementations.

## Rules

When proposing changes:

1. Preserve documentation-first approach.
2. Do not introduce secrets.
3. Do not introduce credentials.
4. Do not introduce recovery codes.
5. Do not introduce vendor lock-in.
6. Prefer concepts over tooling.
7. Prefer architecture over implementation.
8. Preserve recovery-first philosophy.

## Scope

Allowed:

- documentation
- concepts
- templates
- ADRs
- diagrams

Not allowed:

- secret storage
- vault implementation
- IAM implementation
- recovery automation
- credential management

## Source of Truth

Repository documents are the source of truth.

Generated content must remain consistent with:

- Project Specs
- ADRs
- Concepts

## Decision Process

Proposal
→ Pull Request
→ Review
→ Merge

No direct implementation decisions.
