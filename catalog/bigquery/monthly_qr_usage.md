| source_system | asset_type | owner | last_refreshed |
| :--- | :--- | :--- | :--- |
| Google BigQuery | Table | BI Team | 2025-07-02T01:07:00Z |

# Monthly QR Usage

**Business Description:** This table tracks the monthly store level Beep QR usage out of all In store transactions (In Store includes both Beep QR and POS (Point of Sale) offline transactions).

### Schema

| Field Name (API) | Label | Data Type | Description | Possible Values | Is Primary Key | Is Foreign Key | Related Table | Related Field | Data Classification | Notes / Caveats |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **business** | Business | STRING | The business account name. | n/a | TRUE | FALSE | n/a | n/a | Confidential | n/a |
| **storeid** | Store ID | STRING | The store ID associated with a business account. A single business can have multiple store IDs. | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **month** | Month | DATE | Represents the first day of the month for which the data is aggregated (e.g., 2025-06-01 for all of June 2025). | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **instore\_txn** | In-Store Txn | INTEGER | The total count of all successful in-store transactions. This is a combined metric that includes both Beep QR and POS (Point of Sale) offline transactions. | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **instore\_gmv** | In-Store GMV | FLOAT | The total Gross Merchandise Value (in MYR) corresponding to all successful in-store transactions (instore_txn). | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **qrtxn** | QR Txn | INTEGER | The total count of successful Beep QR transactions for the given month and business. | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **qrgmv** | QR GMV | FLOAT | The total Gross Merchandise Value (in MYR) from all successful Beep QR transactions, corresponding to the given month and business. | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **qr\_usage\_gmv** | QR Usage GMV | FLOAT | The percentage share of QR based GMV compared to the total in-store GMV. Formula: `total_qr_gmv / instore_gmv` | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
| **qr\_usage\_txn** | QR Usage Txn | FLOAT | The percentage share of QR-based transactions compared to the total number of in-store transactions. Formula: `total_qr_txn / instore_txn` | n/a | FALSE | FALSE | n/a | n/a | Confidential | n/a |
