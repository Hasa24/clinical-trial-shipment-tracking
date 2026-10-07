# User Stories with Acceptance Criteria

| # | As a... | I want to... | So that... | Acceptance criteria |
|---|---|---|---|---|
| 1 | Supply planner | see all in-transit shipments with status | I can spot delays early | List shows shipment ID, destination, status, ETA; filterable by status |
| 2 | Supply planner | get an alert when a shipment is delayed | I can act before the site runs out of drug | Alert fires when ETA slips past a set threshold; shows the shipment and the reason |
| 3 | Depot manager | see a dispatch queue with packing requirements | I pack the right temperature setup | Each order shows the temperature range and packaging type |
| 4 | Depot manager | mark a shipment as dispatched | status updates for everyone | Status changes to "In transit" with a timestamp and user |
| 5 | Site coordinator | see the ETA for my site's shipments | I can plan receipt | ETA visible without emailing the depot |
| 6 | Site coordinator | confirm delivery and condition | the record is complete | Confirmation captures date, time, and received/damaged flag |
| 7 | QA reviewer | view the temperature log for each shipment | I can decide if the product is usable | Log shows min/max temperature and any excursion periods |
| 8 | QA reviewer | see an audit trail for each exception | quality reviews are documented | Each exception records who, what, when, and the resolution |
| 9 | Supply planner | get an alert on a temperature excursion | the product can be quarantined fast | Alert fires when the reading leaves the allowed range |
| 10 | Product owner | see exceptions by type | I can prioritize fixes | Report groups exceptions (delay, excursion, customs hold) by count |
