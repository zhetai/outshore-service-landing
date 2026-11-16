# Security Policy

## Scope

This repository is a static, single-file landing page plus demo assets. `index.html`
makes no network requests and ships no third-party code: no fonts, CDNs, analytics, or
trackers are loaded at runtime.

## What this repository never contains

- API keys, tokens, passwords, or private keys
- Client names, contracts, or any original evidence-chain material
- Off-platform contact details (email addresses, phone numbers, messaging IDs)
- Personal data of any kind

## Reporting

If you believe you have found a security issue in this repository, please report it
privately through GitHub's **Security → Report a vulnerability** flow instead of opening a
public issue. Please include a short description and, if possible, the steps to reproduce.

Reports are reviewed on a best-effort basis. Because the page is static and collects no
data, the realistic risk surface is limited to content mistakes (for example a leaked
contact detail) rather than runtime vulnerabilities.

## Supported versions

Only the current `main` branch receives fixes.
