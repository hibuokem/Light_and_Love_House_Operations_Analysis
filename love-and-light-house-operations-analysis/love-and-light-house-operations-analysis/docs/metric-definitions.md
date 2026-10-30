# Metric definitions and interpretation

The definitions below follow the Excel workbook's analysis notes.

| Metric | Definition used in the workbook |
|---|---|
| On-time delivery | `Delivery_Days <= Promised_Days` |
| Late delivery | `Delivery_Days > Promised_Days` |
| On-time rate | Orders marked on time divided by all 1,800 cleaned orders |
| Late rate | Orders marked late divided by all 1,800 cleaned orders |
| Cancellation rate | Cancelled orders divided by all 1,800 cleaned orders |
| Return rate | Returned orders divided by all 1,800 cleaned orders |
| Average delivery days | Average of valid, non-negative delivery-day values |
| Average rating | Average of available customer ratings; blank ratings are excluded, not converted to zero |

## Data-quality decisions

- Preserve the supplied raw records in `Raw_Data`.
- Remove 12 exact duplicate rows from `Cleaned_Data`.
- Retain missing region and acquisition-channel values as blank rather than inventing values.
- Retain missing customer ratings as blank.
- Recalculate late status from actual versus promised delivery days because the supplied late-delivery field contained 227 logic mismatches.
- Validate delivery type, order status, promised days, and delivery days against the checks recorded in `Data_Quality`.

## Reading the results carefully

Some regional pivot summaries contain 1,790 records because the 10 records with missing region values cannot be assigned to a named region. Overall KPI calculations use all 1,800 cleaned orders. The relationship between delivery performance and customer ratings is observational; it does not demonstrate cause and effect. The priority-matrix thresholds are analyst-defined triage rules, not externally validated service standards.
