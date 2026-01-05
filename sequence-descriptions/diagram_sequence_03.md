# Sequence Diagram Description: View Book Details

**Diagram File**: `diagram_sequence_03.jpg`

## 1. Use Case Name
**View Book Details & Reviews**

## 2. Actors Involved
- **Customer**
- **UI** (Book Details Page)
- **System**
- **Book Service**
- **Review Service**
- **Database**

## 3. Pre-conditions
- User has selected a specific book from the catalog.

## 4. Post-conditions
- User views detailed info, reviews, and related books.
- User may submit a new review.

## 5. Step-by-Step Interaction Flow

### Main Flow: Load Details
1.  **Customer** selects a book.
2.  **UI** calls `Get Book Details` on **System**.
3.  **System** fetches book data via **Book Service** -> **Database**.
4.  **System** fetches reviews via **Review Service** (Note: Review data likely stored in Database, accessed via Service).
5.  **UI** displays full book info.

### Sub-process: Related Books (Loop)
1.  **UI** requests related books (e.g., same genre).
2.  **System** uses **Book Service** to query **Database** for related items.
3.  Returned list is displayed on the UI.

### Sub-process: Submit Review (Alt)
1.  **Customer** writes a review.
2.  **UI** submits review to **System**.
3.  **System** -> **Database** saves the review.
    -   **Success**: UI shows "Review Added".
    -   **Failure**: UI shows error message.

## 6. System Behavior Explanation
This diagram highlights the use of micro-services or distinct service layers (**BookService** vs **ReviewService**) to compose a single page view. It handles complex data aggregation (Details + Reviews + Related) seamlessly.

## 7. Conclusion
Ensures a rich user experience by aggregating all necessary context for a product decision (purchase) into one view.
