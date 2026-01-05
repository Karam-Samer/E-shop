# Sequence Diagram Description: Admin Book Management

**Diagram File**: `diagram_sequence_06.jpg`

## 1. Use Case Name
**Admin: Manage Books (CRUD)**

## 2. Actors Involved
- **Admin**: Privileged user.
- **UI** (Admin Panel).
- **System**.
- **Book Service**.
- **Database**.

## 3. Pre-conditions
- User is logged in as Admin.

## 4. Post-conditions
- The book catalog is updated (Item added, deleted, or modified).

## 5. Step-by-Step Interaction Flow

### Scenario A: Add Book
1.  **Admin** enters book data.
2.  **System** -> **Book Service** validates data.
3.  **Book Service** inserts new book into **Database**.
4.  **UI** shows "Book Added Successfully".

### Scenario B: Delete Book
1.  **Admin** selects a book to delete.
2.  **System** requests deletion.
3.  **Database** removes the record.
4.  **UI** confirms deletion.

### Scenario C: Update Book
1.  **Admin** selects book to edit.
2.  **System** retrieves current data for display.
3.  **Admin** submits changes.
4.  **System** updates record in **Database**.
5.  **UI** shows "Book Updated".

## 6. System Behavior Explanation
Provides full Create-Read-Update-Delete (CRUD) capabilities for the inventory. It utilizes the **Book Service** for business logic (validation) before interacting with the storage.

## 7. Conclusion
Enables platform administrators to maintain the product catalog efficiently.
