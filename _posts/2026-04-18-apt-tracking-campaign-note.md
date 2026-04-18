---
title: "APT Tracking: Campaign Delta Note (Q2 Snapshot)"
layout: post
date: 2026-04-18 10:30:00 +0530
categories: [apt-tracking]
tags: [apt, campaign, mitre, c2]
description: "How to document campaign changes quickly and keep your tracking page operationally useful."
---

## Executive Summary

This note captures shifts in initial access and C2 hosting behavior observed in a recurring intrusion cluster.

## Observed Changes

- Initial access shifted from macro-heavy lures to archive-plus-script delivery.
- C2 moved to shorter-lived VPS hosts with domain rotation every few days.
- Post-exploitation favored native admin tools over dropping many binaries.

## ATT&CK Highlights

- `T1566` Phishing
- `T1059` Command and Scripting Interpreter
- `T1071` Application Layer Protocol

## Analyst Notes

The key tracking metric is not volume of IOCs but stability of operator behavior over time. Keep one-page delta summaries for every campaign checkpoint.

