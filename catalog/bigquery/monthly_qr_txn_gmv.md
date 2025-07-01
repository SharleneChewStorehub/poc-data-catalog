| source_system | asset_type | owner | last_refreshed |
| :--- | :--- | :--- | :--- |
| Google BigQuery | Table | BI Team | 2025-07-01T17:00:00Z |

# Monthly QR Txn & GMV

**Business Description:** This table tracks monthly store level Beep QR transaction count and GMV, as well as the store's first Beep QR transaction date and year-month.

### Schema

| Field Name (API) | Label | Data Type | Description | Possible Values | Is Primary Key | Is Foreign Key | Related Table | Related Field | Data Classification | Notes / Caveats |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **month** | Month | DATE | Represents the first day of the month for which the data is aggregated (e.g., 2025-06-01 for all of June 2025). | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **country** | Country | STRING | The country of the business. | 'MY', 'TH', 'PH' | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **cb\_status** | CB Status | STRING | The subscription status of the business account. | 'active', 'cancelled', 'non_renewing' | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **business** | Business | STRING | The business account name. | n/a | TRUE | FALSE | n/a | n/a | Confidential | n/a |
| **storeid** | Store ID | STRING | The store id associated with a business account. A single business can have multiple store IDs. | n/a | FALSE | FALSE | n/a | n/a | Confidential | Can be connected to store id from other tables. |
| **firstqr** | First QR | DATE | The exact date of the first successful Beep QR transaction recorded for the given store or business. | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **firstqr\_month** | First QR Month | DATE | The month of the first successful Beep QR transaction, represented as the first day of that month (e.g. 2025-06-01). This field is derived from firstqr and is used for monthly aggregation and reporting. | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **qrtxn** | QR Txn | INTEGER | The total count of successful Beep QR transactions for the given month and business. | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **qrgmv** | QR GMV | FLOAT | The total Gross Merchandise Value (in MYR) from all successful Beep QR transactions, corresponding to the given month and business. | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
