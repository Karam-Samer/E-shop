# Sequence Diagram Description: Cart Management

**Diagram File**: `diagram_sequence_04.jpg`

## 1. Use Case Name
**Manage Shopping Cart**

## 2. Actors Involved
- **Customer**
- **UI** (Cart Page)
- **System**
- **Cart Service**
- **Book Service** (for availability check)
- **Database**

## 3. Pre-conditions
- User is browsing books or viewing the cart.

## 4. Post-conditions
- Cart is updated (item added/removed) or User is informed of stock issues.

## 5. Step-by-Step Interaction Flow

### Scenario A: View Cart
1.  **Customer** opens cart.
2.  **System** -> **Cart Service** -> **Database** retrieves current cart items.
3.  **UI** displays the cart.

### Scenario B: Add Book to Cart
1.  **Customer** adds a book.
2.  **System** calls **Book Service** to `Check Availability`.
3.  **Book Service** queries **Database** for stock.
    -   **If In Stock**:
        4.  **Cart Service** inserts book into **Database**.
        5.  **System** returns "Updated Cart".
        6.  **UI** displays updated cart.
    -   **If Out of Stock**:
        4.  **System** returns "Unavailable".
        5.  **UI** shows "Out of Stock" error.

### Scenario C: Remove Item
1.  **Customer** removes a book.
2.  **Cart Service** deletes the item from **Database**.
3.  **UI** refreshes the cart view.

## 6. System Behavior Explanation
Crucially, this process includes a **real-time stock check** before adding items, preventing overselling. It delegates logic to a specialized **Cart Service**.

## 7. Conclusion
Provides a robust shopping experience by validating inventory in real-time and allowing flexible cart management.
