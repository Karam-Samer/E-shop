# Sequence Diagram Description: User Authentication

**Diagram File**: `diagram_sequence_01.jpg`

## 1. Use Case Name
**User Login and Registration**

## 2. Actors Involved
- **Customer**: The end-user accessing the website.
- **UI (User Interface)**: The front-end interface (pages/forms).
- **System**: The backend application controller.
- **Database**: The persistent storage for user credentials.

## 3. Pre-conditions
- The user has accessed the website.
- The user is not currently logged in.

## 4. Post-conditions
- **Success**: The user is authenticated and redirected to the home page.
- **Failure**: The user remains on the login/register page with an error message.

## 5. Step-by-Step Interaction Flow

### Scenario A: User Login
1.  **Customer** selects "Login" on the UI.
2.  **Customer** enters `username` and `password`.
3.  **UI** sends the credentials to the **System**.
4.  **System** queries the **Database** to check the user.
5.  **Database** returns `valid` or `invalid` status.
    -   **If Valid**:
        6.  **System** confirms login to **UI**.
        7.  **UI** redirects **Customer** to the Home Page.
    -   **If Invalid**:
        6.  **System** returns a "Login Failed" error.
        7.  **UI** displays the error message to the **Customer**.
        8.  *(Loop)* **Customer** may re-enter credentials to try again.

### Scenario B: User Registration
1.  **Customer** selects "Register".
2.  **Customer** enters registration data (Name, Email, Password, etc.).
3.  **UI** sends data to **System**.
4.  **System** checks **Database** for existing user.
    -   **If User Exists**:
        5.  **Database** returns "User Exists".
        6.  **System** returns "Registration Failed".
        7.  **UI** shows an error message.
    -   **If New User**:
        5.  **System** requests **Database** to insert new user.
        6.  **Database** confirms insertion success.
        7.  **System** confirms registration to **UI**.
        8.  **UI** shows a confirmation message and redirects to Home Page.

## 6. System Behavior Explanation
The system enforces a strict separation of concerns. The **UI** handles data entry and display, while the **System** (Backend) orchestrates the logic. The **Database** is only accessed by the System, ensuring security. The diagram illustrates both success and failure paths using `alt` blocks, ensuring robust error handling.

## 7. Error Handling
- **Invalid Login**: The system catches invalid credentials and prompts a retry loop.
- **Duplicate Registration**: The system prevents creating multiple accounts with the same credentials.

## 8. Conclusion
This sequence diagram defines a secure and user-friendly authentication process, covering both entry points (Login and Register) and handling common edge cases like incorrect passwords or existing accounts.
