# Data Requirements

## Shipment
| Field | Description | Example |
|---|---|---|
| shipment_id | Unique ID | SHP-00123 |
| study_id | Trial the drug belongs to | STUDY-A |
| site_id | Destination trial site | SITE-045 |
| product | Investigational product name | Drug X 10 mg |
| temperature_range | Allowed range | 2-8°C |
| status | Created / Packed / In transit / Delivered / On hold | In transit |
| dispatch_time | When it left the depot | 2026-10-01 09:00 |
| eta | Expected arrival | 2026-10-03 14:00 |
| delivered_time | Actual arrival | 2026-10-03 13:20 |
| received_condition | Received OK / Damaged | Received OK |

## Temperature log
| Field | Description |
|---|---|
| shipment_id | Links to shipment |
| timestamp | Reading time |
| temperature_c | Reading in °C |
| excursion_flag | True if outside allowed range |

## Exception
| Field | Description |
|---|---|
| exception_id | Unique ID |
| shipment_id | Links to shipment |
| type | Delay / Temperature excursion / Customs hold |
| raised_time | When detected |
| owner | Person responsible |
| resolution | What was decided |
| resolved_time | When closed |

## Users and roles
Supply planner, Depot manager, Site coordinator, QA reviewer, Product owner. Each role sees only the screens and actions relevant to it.

## Business rules
- Any reading outside the allowed range sets excursion_flag and raises an alert.
- A shipment cannot be marked Delivered until the site coordinator confirms condition.
- Every exception must have an owner and a resolution before it can be closed.
