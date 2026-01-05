# Sequence Diagram Description: Explore Books

**Diagram File**: `diagram_sequence_02.jpg`

## 1. Use Case Name
**Explore and Search Books**

## 2. Actors Involved
- **Customer**: The user browsing the catalog.
- **UI**: The "Explore Books" page.
- **System**: Backend controller.
- **Book Service**: Specialized service for book logic.
- **Database**: Storage for book inventory.

## 3. Pre-conditions
- User is on the website (authentication not strictly required for browsing).

## 4. Post-conditions
- The user views a list of books or search results.

## 5. Step-by-Step Interaction Flow

### Scenario A: View All Books (Initial Load)
1.  **Customer** opens "Explore Books" page.
2.  **UI** requests books from **System**.
3.  **System** forwards request to **Book Service**.
4.  **Book Service** queries **Database**.
5.  **Database** returns the book list.
6.  **Book Service** -> **System** -> **UI** propagate the book data.
7.  **UI** displays the books to the **Customer**.

### Scenario B: Pagination (Loop)
1.  **Customer** requests the next page (Load multiple pages).
2.  **UI** requests the next set of books.
3.  **System** delegations to **Book Service** and **Database**.
4.  Data is returned and displayed to the user.

### Scenario C: Search (Alt)
1.  **Customer** enters a search keyword.
2.  **UI** sends "Search Books" request to **System**.
3.  **System** -> **Book Service** -> **Database** execute the query with the keyword.
4.  **Database** returns filtered results.
5.  **UI** displays the specific search results.

## 6. System Behavior Explanation
The system uses a **Book Service** as an intermediary, promoting a modular architecture. It supports lazy loading or pagination (represented by the `loop` fragment) to handle large datasets efficiently.

## 7. Conclusion
This diagram illustrates the core browsing functionality, ensuring users can efficiently navigate the catalog through pagination and targeted search.
