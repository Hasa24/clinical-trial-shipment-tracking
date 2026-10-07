# Clinical Trial Shipment Tracking: Problem Statement

**Note:** This is an independent case study based on a fictional scenario, not any company's real system.

## Background
A pharma company supplies investigational drug products to clinical trial sites in many countries. Many products need controlled temperatures (e.g., 2-8°C), and a damaged or late shipment can delay patient dosing or invalidate trial material.

## Problem
- Supply planners have no single view of where shipments are.
- Temperature excursions are found only after arrival, when the product may already be unusable.
- Site coordinators email the depot to ask for status, which wastes time.
- Exceptions (delays, customs holds, excursions) are tracked in spreadsheets, so there is no audit trail for quality review.

## Goal
Give stakeholders real-time visibility of each shipment, automatic alerts on delays and excursions, and a documented exception-handling workflow.

## Scope
**In scope:** Shipment status tracking, temperature monitoring alerts, exception logging, delivery confirmation.

**Out of scope:** Manufacturing, patient-level dosing, inventory forecasting.

## Success measures
- Fewer status-request emails from sites
- Faster response to excursions
- 100% of exceptions logged with an owner and resolution

## Stakeholders

| Stakeholder | Role | What they need |
|---|---|---|
| Supply planner | Plans and releases shipments | See all in-transit shipments and delays at a glance |
| Depot manager | Packs and dispatches | Clear dispatch queue and packing requirements |
| Site coordinator | Receives drug at the trial site | Accurate ETA and delivery confirmation |
| QA / quality reviewer | Decides if a product is usable | Temperature log and full audit trail per shipment |
| Courier / logistics partner | Transports the shipment | Clear handover and exception procedures |
| IT / product owner | Builds the solution | Prioritized, testable requirements |
