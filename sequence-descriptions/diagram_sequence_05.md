# Sequence Diagram Description: Checkout Process

**Diagram File**: `diagram_sequence_05.jpg`

## 1. Use Case Name
**Checkout and Payment**

## 2. Actors Involved
- **Customer**
- **UI**
- **System**
- **Checkout Service**
- **Payment Service**
- **Database**

## 3. Pre-conditions
- User has items in the cart and initiates checkout.

## 4. Post-conditions
- Order is placed and saved in history.
- Cart is cleared (implied).

## 5. Step-by-Step Interaction Flow

1.  **Customer** clicks "Checkout".
2.  **System** -> **Checkout Service** prepares the order (calculates totals, loads cart data from **Database**).
3.  **UI** shows Order Summary.
4.  **Customer** chooses Payment Method and confirms.
5.  **System** delegates to **Payment Service** to process transaction.
    -   **If Payment Successful**:
        6.  **System** calls `Save Order`.
        7.  **Checkout Service** -> **Database** inserts the order.
        8.  **UI** shows "Order Confirmation".
    -   **If Payment Failed**:
        6.  **System** returns failure status.
        7.  **UI** shows "Payment Error".

## 6. System Behavior Explanation
Separates **Checkout Logic** (order assembly) from **Payment Processing** (financial transaction). This ensures that orders are only persisted to the database *after* a successful payment confirmation.

## 7. Conclusion
The critical financial transaction phase of the application, ensuring data integrity and user feedback on transaction status.
