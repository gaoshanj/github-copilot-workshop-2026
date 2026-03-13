# Order Processing System Requirements

## Overview
Build a backend module to handle customer orders.

## Functional Requirements
1.  **Create Order**:
    -   Input: User ID, List of Product IDs and Quantities.
    -   Validation: Check stock availability.
    -   Action: Deduct stock, create order record, calculate total price.
2.  **Order Status**:
    -   Initial status: `PENDING`.
    -   After payment (mocked): `PAID`.
    -   After shipping: `SHIPPED`.
3.  **History**:
    -   User can view their past orders.

## Technical Requirements
-   Language: Python (FastAPI) or Node.js (Express).
-   Database: SQLite (for demo purposes).
-   Architecture: RESTful API.
