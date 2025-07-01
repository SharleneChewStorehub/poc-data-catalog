| source_system | asset_type | owner | last_refreshed |
| :--- | :--- | :--- | :--- |
| Google BigQuery | Table | BI Team | 2025-07-02T01:11:51+08:00 |

# Monthly QR Payment Method

**Business Description:** This table tracks the monthly business (account) level Beep QR transactions breakdown by the payment method (Offline or Online).

### Schema

| Field Name (API) | Label | Data Type | Description | Possible Values | Is Primary Key | Is Foreign Key | Related Table | Related Field | Data Classification | Notes / Caveats |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **month** | Month | DATE | Represents the first day of the month for which the data is aggregated (e.g., 2025-06-01 for all of June 2025). | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **business** | Business | STRING | Business Account Name. | n/a | FALSE | n/a | n/a | n/a | Confidential | n/a |
| **paymentmethod** | Payment Method | STRING | Specifies the transaction channel. | 'Online', 'Offline' | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **total\_qr\_txn** | Total QR Txn | INTEGER | The total count of successful Beep QR transactions for the given month and business. | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **total\_qr\_gmv** | Total QR GMV | FLOAT | The total Gross Merchandise Value (in MYR) from all successful Beep QR transactions, corresponding to the given month and business. | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
