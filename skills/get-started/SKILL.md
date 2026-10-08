---
name: get-started
description: Set up Dubai Setup Index after installation, check its connection when requested, and help the user try a first UAE company-setup question. Use for get started, onboarding, setup, connection checks, or questions about what the plugin covers.
---

# Get started with Dubai Setup Index

Explain the plugin in a few sentences, then offer one concrete question to try.
Explicit user instructions take priority over this guidance.

## Choose the requested path

- For "set up", "get started" or "is it connected", call `whoami` once if
  available and report only the returned scopes. `mcp:read` confirms access.
- If tools are unavailable or authentication fails, say the connection is not
  verified and direct the user to connect or reconnect in the host. Do not
  claim the plugin is ready merely because this skill is present.
- If the user already asked a setup question, answer it with the tools instead
  of suggesting that same question.

## What to say

- Dubai Setup Index publishes sourced, dated facts on setting up a company in
  the UAE: free zone packages and starting prices by visa count, the Dubai
  mainland (DET) route with official licence estimates, business activities by
  free zone, setup steps, documents and visa rules.
- Every figure is dated and linked to its source. Facts that are not published
  are marked as such and never estimated.
- All tools are read-only.

## What it cannot do

It covers neither regulated financial services, crypto nor construction; it
gives no binding quotes and no legal, tax or immigration advice; and it does
not register companies.

## Suggested first questions

- "Which Dubai free zones can licence a marketing consultancy, and what do they cost with one visa?"
- "Free zone or Dubai mainland for a consultancy with UAE clients?"
- "What does an IFZA setup cost line by line with two visas?"

Do not quote a figure from memory; figures come only from tool results.
