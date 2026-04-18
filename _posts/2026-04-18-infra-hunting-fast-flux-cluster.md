---
title: "Infra Hunting: Fast-Flux Cluster Triage Workflow"
layout: post
date: 2026-04-18 10:00:00 +0530
categories: [infra-hunting]
tags: [dns, infrastructure, hunting, pivoting]
description: "A practical process to pivot from one suspicious domain into a wider fast-flux cluster."
---

## TL;DR

This workflow starts from one suspicious domain and expands quickly using passive DNS, TLS overlap, and hosting artifacts to identify related infrastructure.

## Starting Artifact

- Seed domain: `update-security-check[.]com`
- Trigger: unusual DNS churn and short TTL values

## Pivot Strategy

1. Collect passive DNS history for the last 30 days.
2. Group by recurring IPs and ASN.
3. Pivot into certificates reused across adjacent domains.
4. Score candidates by overlap count and recent activity.

## What Worked

- Shared certificate Subject Alternative Name overlap was the strongest signal.
- WHOIS fields were low value due to privacy masking.

## Detection Opportunity

Alert on domains with:

- TTL under 300 seconds over repeated windows
- More than 5 unique A records in 24 hours
- Certificate overlap with known suspicious cluster

