# Ujima Digital Pride: Multi-Agent Credit Triage Simulator

## SASRA & Central Bank of Kenya (CBK) Compliant • Built for Kenya DPA 2022

Ujima is a cooperative multi-agent credit scoring and financial inclusion framework designed specifically for Sub-Saharan savings groups (SACCOs) and informal market traders. By shifting credit evaluation away from rigid, westernized monthly salary assumptions, Ujima aligns risk assessment with seasonal agricultural flushes and trading cycles.

This repository contains the interactive Phase 4 Multi-Agent Triage Simulator, which showcases the automated workflow, safety guardrails, and data sovereignty compliance layers required under modern East African regulations.

## 🌾 The Problem: The Urban Bias in Standard Credit Scoring

Traditional credit bureaus and automated mobile lend-techs enforce flat, monthly repayment schedules. In East Africa, over 80% of informal traders and smallholders experience highly cyclical cash flows driven by crop harvest windows (such as the Matooke harvests in March/April and September/October, or Maize harvests in October/November).

When standard scoring engines misinterpret low-cash planting seasons as static default risk:

Informal traders face a 68% credit denial rate compared to just 22% for formal employees.

Traders are pushed toward predatory, unregulated mobile loan sharks.

Local cooperative capital (SACCO) remains under-utilized.

## 🦁 The Solution: The Three-Agent Pride (RANK)

The simulation represents a coordinated multi-agent "ambush" designed to safely ingest informal conversational logs and USSD ledger trails, matching them to regional harvest data:

### 1. Scout Agent (Financial Literacy Coach)

Role (R): Frontline outreach and conversational education. Aligns household financial planning with crop cycles.

Action Limits (A): Restricts outputs to a maximum of 3 outbound SMS/USSD pushes per day. Programmed to never suggest specific high-yield debt products.

Notification Triggers (N): Instantly alerts the Guardian Agent if a member mentions predatory entities ("loan shark", "threatens", "seize").

Kill Switch (K): Members can send *#700# via USSD to freeze all automated outbound messages instantly.

### 2. Guardian Agent (Loan Triage Guard)

Role (R): Run real-time automated scoring and pipeline bias audits.

Action Limits (A): Direct auto-approvals are strictly capped at KES 15,000. Rejections require a minimum of 3 distinct risk metrics.

Notification Triggers (N): Automatically flags files for manual human coordination if the applicant supports dependents under 5 years of age.

Kill Switch (K): Direct override via admin token or USSD *#733# freezes automated decision algorithms.

### 3. Hunter Agent (Human-in-the-Loop Coordinator)

Role (R): Context-broker that matches high-stress or borderline applicants with specialized human credit officers.

Action Limits (A): Purely operational; strictly forbidden from issuing automated approvals or rejections.

Notification Triggers (N): Immediately dispatches comprehensive background briefs to the matched officer's field terminal.

Kill Switch (K): Administrative system-wide freeze command via *#799#.

## 🛡️ Sovereign Data Stewardship (O.A.S.I.S. Protocol)

To comply with the Kenya Data Protection Act (DPA) 2022, the system enforces strict structural isolation:

Sovereign Hosting: All micro-enterprise cash ledgers and conversation logs are pinned to the AWS Africa (Cape Town) infrastructure.

Rule 1 Directory Constraints: * Public Metadata (Anonymized Logs): Routed strictly through /artifacts/{appId}/public/data/

Private PII (Encrypted Financial States): Nested securely in /artifacts/{appId}/users/{userId}/

k-Anonymity Guard: Aggregates regional identity groups where $k \ge 5$ to prevent individual tracking in sparsely populated rural wards.

Auto-Deletion: Implements a strict 180-day automated purge loop on cold metadata.

## 💻 Quick Start: Running the Simulator

The simulator is self-contained within a single, highly responsive file (ujima_live_simulator.html).

Download or clone this repository.

Locate the ujima_live_simulator.html file.

Open it in any modern web browser (no local web server or terminal dependencies required).

Simulating Scenarios

Use the left control panel to select different predefined profiles:

Grace (Maize Farmer): High alignment. Cashflow peaks in October/November. Triggers clean automated verification.

Aminata (Shea Butter Vendor): Irregular cashflow across border zones. Triggers human escalations via the Hunter Agent to prevent trade bottlenecks.

Joshua (Matooke Trader): Mentions loan shark threats. Triggers emergency Scout flags, immediately invoking the PRIDE human triage loop to ensure borrower protection.
