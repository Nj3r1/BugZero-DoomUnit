 Defect Log Summary Table

## 3.Defect Log Summary Table

| Defect ID | Defect Title/Summary                                               | Feature               | Sub-Feature               | Severity | Priority | Status | Reported By            | Date Reported | 
| :-------- | :------------------------------------------------------------------| :-------------------- | :------------------------ | :------- | :------- | :----- | :--------------------- | :------------ | 
| BUG001    | User registration accepts weak passwords                           | User Authentication   | Registration              | Critical | P1       | New    | Susan Ng’ang’a         | 2025-07-07    |           
| BUG002    | Invalid email format is accepted during registration               | User Authentication   | Registration              | Critical | P1       | New    | Susan Ng’ang’a         | 2025-07-07    |           
| BUG003    | Filter by Status shows incorrect orders (pending shows missed)     | Admin Functions       | Request Filtering         | Critical | P1       | New    | Susan Ng’ang’a         | 2025-07-07    |           
| BUG004    | New registered users do not reflect on system dashboard            | User Management       | User Data Display         | Medium   | P2       | New    | Susan Ng’ang’a         | 2025-07-07    |           
| BUG005    | Logging out redirects to the request pickup page                   | User Authentication   | Logout                    | Medium   | P2       | New    | S. Ng’ang’a, T. Waweru | 2025-07-07    |           
| BUG006    | After registration, user is not automatically logged in/redirected | User Authentication   | Registration Flow         | Medium   | P2       | New    | Susan Ng’ang’a         | 2025-07-07    |           
| BUG007    | Filter by Status shows incorrect orders (pending shows missed)     | Admin Functions       | Request Filtering         | Medium   | P2       | New    | Susan Ng’ang’a         | 2025-07-07    |           
| BUG008    | Filter by Location is not working as expected (shows wrong users)  | Admin Functions       | Request Filtering         | Medium   | P2       | New    | Susan Ng’ang’a         | 2025-07-07    |           
| BUG009    | Filter by Location is not working as expected (shows wrong users)  | Admin Functions       | Request Filtering         | Critical | P1       | New    | Susan Ng’ang’a         | 2025-07-07    |           
| BUG010    | Awareness page layout overlap / Page does not respond to click     | Content Features / UI | Page Display / Navigation | Low      | P3       | New    | Susan Ng’ang’a         | 2025-07-07    |           
| BUG011    | Register tab is not highlighting on navigation                     | Usability / UI        | Navigation Highlighting   | Low      | P3       | New    | Susan Ng’ang’a         | 2025-07-07    |           







4. Detailed Defect Descriptions

---
4.1. Defect ID: BUG001
Defect Title: Accepts weak passwords

Description: The user registration process allows users to create accounts with passwords that are considered weak, lacking proper complexity requirements. This poses a significant security risk.

Expected Behavior: The system should enforce strong password policies. It should reject passwords that do not meet predefined strength criteria and display specific, actionable error messages.

Actual Behavior: The system accepts weak passwords like "password123" during user registration. Subsequently, the user is successfully able to log in to the application using these insecure credentials.

Steps to Reproduce:

Navigate to the user Registration page.

Enter valid details for the Email and Username fields.

In the "Password" and "Confirm Password" fields, enter a weak password .

Click the "Submit" or "Create Account" button to complete registration.

Observe that the registration is accepted, and the user can then successfully log in with the weak password.

Environment:

OS: Windows 11

Browser/Device: Chrome 120, Samsung A22

App Version: v2.5.0

Test Data: User: user@cleancity.com / Password: password123

---

4.2. Defect ID: BUG002
Defect Title: Invalid Email is accepted during registration

Description: The registration form's email input field lacks proper validation for email format, allowing users to register with syntactically incorrect or malformed email addresses.

Expected Behavior: The registration process should strictly validate the email format. It should reject invalid email addresses with a clear error message.

Actual Behavior: Registration is accepted even when an invalid email format is provided. No error message related to the email's format is displayed, and an account is created with the malformed email.

Steps to Reproduce:

Navigate to the user Registration page.

Enter an invalid email address in the email field.

Enter valid details for Username, Password, and Confirm Password.

Click the "Submit" or "Create Account" button.

Observe that registration is accepted without any email format validation error.

Environment:

OS: Windows 11, Windows 11 Pro

Browser/Device: Chrome 120, Samsung A22, Redmi 13C

App Version: v2.5.0

Test Data: User: user@cleancity.com / Password: password123 

---

4.3. Defect ID: BUG003
Defect Title: Filter by status does not respond correctly (shows missed orders with pending)

Description: When an administrator attempts to filter pickup requests by "Pending" status, the system incorrectly displays "Missed" orders alongside the actual pending orders.

Expected Behavior: The "Filter by Status" dropdown, when "Pending" is selected, should precisely filter the list to only display pickup orders that are currently in a "Pending" status.

Actual Behavior: When the "Filter by Status" dropdown is used and "Pending" is chosen, the displayed results include both orders with a "Pending" status and orders with a "Missed" status.

Steps to Reproduce:

Navigate to the administrative section for managing pickup requests (e.g., Admin Dashboard > Manage Pickups).

Locate the "Filter by Status" dropdown menu.

Select "Pending" as the desired status from the dropdown.

Click the "Filter" or "Apply Filter" button (if present).

Observe the displayed list of orders; it will incorrectly contain orders with "Missed" status in addition to "Pending" ones.

Environment:

OS: Windows 11

Browser/Device: Chrome 120, Samsung A22

App Version: v2.5.0

Test Data: User: user@cleancity.com / Password: password123 

---

4.4. Defect ID: BUG004
Defect Title: New Registered users do not reflect on system dashboard / User information not found after login

Description: After a new user successfully registers and subsequently logs into the system, their personal information or any user-specific data is not accessible or visible on their dashboard or profile pages.

Expected Behavior: When a new user is registered and successfully logs in, they should be able to access and view their own personalized information, profile details, and any data relevant to their account on the system dashboard.

Actual Behavior: Upon successful registration and login, the user is unable to find or access their own information on the system dashboard or their personal profile section.

Steps to Reproduce:

Navigate to the user Login page.

Register a new user account with valid credentials.

Log in to the application using the newly created user account.

Navigate to the user dashboard or profile page.

Observe that the user's information (e.g., username, email, scheduled pickups) is not displayed or accessible.

Environment:

OS: Windows 11

Browser/Device: Chrome 120, Samsung A22

App Version: v2.5.0

Test Data: User: user@cleancity.com / Password: password123

---

4.5. Defect ID: BUG005
Defect Title: Logging out leads to the request pickup page instead of login page

Description: When a user performs the logout action, they are incorrectly redirected to the "Request Pickup" scheduler page, which is typically an authenticated page, instead of the expected login page or application homepage.

Expected Behavior: Upon successful logout, the user should be redirected to the application's login page, the public homepage, or a dedicated logout confirmation page, clearly indicating that their session has been terminated and they are no longer logged in.

Actual Behavior: After clicking the "Logout" button, the system displays the "Request Pickup" scheduler page. This behavior is unexpected and might imply the session is not fully terminated or exposes an authenticated page to a logged-out user.

Steps to Reproduce:

Navigate to any page where the user is currently logged in .

Locate and click the "Logout" button or link.

Observe the page that is displayed immediately after clicking "Logout"; it will be the "Pickup Scheduler" page.

Environment:

OS: Windows 11

Browser/Device: Chrome 120, Samsung A22

App Version: v2.5.0

Test Data: User: user@cleancity.com / Password: password123

---

4.6. Defect ID: BUG006
Defect Title: After registration, page does not automatically log in or redirect to dashboard

Description: Following a successful user registration, the system displays a "Registration Successful" message, but it fails to automatically log in the newly created user or redirect them to their personalized dashboard/home page. The user remains on the registration page.

Expected Behavior: Upon successful account creation, the system should either automatically log in the user and redirect them to their dashboard, or redirect them to the login page with a clear success message, prompting them to log in manually.

Actual Behavior: After completing the registration form and clicking "Create Account," a "Registration Successful" message appears, but the browser remains on the registration page. The user is not automatically logged in or redirected.

Steps to Reproduce:

Navigate to the user Registration page.

Key in all required valid details (Email, Username, Password, Confirm Password).

Click on the "Create Account" button.

Observe that a "Registration Successful" message is displayed, but the page does not navigate away; it remains on the registration page.

Environment:

OS: Windows 11

Browser/Device: Chrome 120, Samsung A22

App Version: v2.5.0

Test Data: User: user@cleancity.com / Password: password123

---

4.7. Defect ID: BUG007
Defect Title: Filter by status does not respond correctly (shows missed orders with pending)

Description: When an administrator attempts to filter pickup requests by "Pending" status, the system incorrectly displays "Missed" orders alongside the actual pending orders. This leads to inaccurate data representation and potential confusion for administrators.

Expected Behavior: The "Filter by Status" dropdown, when "Pending" is selected, should precisely filter the list to only display pickup orders that are currently in a "Pending" status.

Actual Behavior: When the "Filter by Status" dropdown is used and "Pending" is chosen, the displayed results include both orders with a "Pending" status and orders with a "Missed" status.

Steps to Reproduce:

Navigate to the administrative section for managing pickup requests .

Locate the "Filter by Status" dropdown menu.

Select "Pending" as the desired status from the dropdown.

Click the "Filter" or "Apply Filter" button (if present).

Observe the displayed list of orders; it will incorrectly contain orders with "Missed" status in addition to "Pending" ones.

Environment:

OS: Windows 11

Browser/Device: Chrome 120, Samsung A22

App Version: v2.5.0

Test Data: User: user@cleancity.com / Password: password123 

---

4.8. Defect ID: BUG008
Defect Title: ‘Filter by Location’ is not working as expected 

Description: The "Filter by Location" functionality within the request management section  is not operating as intended. When a specific location is selected as a filter, the system incorrectly displays users or requests that originate from other, non-selected locations.

Expected Behavior: When filtering requests by a specific location ,the system should only display requests or users who have registered or made requests from that exact, specified location.

Actual Behavior: When the "Filter By Location" dropdown is used to select a location , the filtered results include users or requests that are registered under or originate from other, incorrect locations.

Steps to Reproduce:

Navigate to the "Filter Requests" section .

Locate the "Filter By Location" dropdown and choose "Eldoret."

Optionally, apply additional filters such as "Filter by status" (e.g., "all status," "pending," "scheduled," "completed," and "missed").

Observe the displayed list of users/requests; it will incorrectly contain entries from locations other than Eldoret.

Environment:

OS: Windows 11

Browser/Device: Chrome 120, Samsung A22

App Version: v2.5.0

Test Data: User: user@cleancity.com / Password: password123 

---

4.9. Defect ID: BUG009
Defect Title: ‘Filter by Location’ is not working as expected (displays users from other locations)

Description: The "Filter by Location" functionality within the request management section  is not operating as intended. When a specific location  is selected as a filter, the system incorrectly displays users or requests that originate from other, non-selected locations.

Expected Behavior: When filtering requests by a specific location , the system should only display requests or users who have registered or made requests from that exact, specified location.

Actual Behavior: When the "Filter By Location" dropdown is used to select a location ,the filtered results include users or requests that are registered under or originate from other, incorrect locations.

Steps to Reproduce:

Navigate to the "Filter Requests" section

Locate the "Filter By Location" dropdown and choose "Eldoret."

Optionally, apply additional filters such as "Filter by status" (e.g., "all status," "pending," "scheduled," "completed," and "missed").

Observe the displayed list of users/requests; it will incorrectly contain entries from locations other than Eldoret.

Environment:

OS: Windows 11

Browser/Device: Chrome 120, Samsung A22

App Version: v2.5.0

Test Data: User: user@cleancity.com / Password: password123 

---

4.10. Defect ID: BUG010
Defect Title: Awareness page layout overlap / Page does not respond to click

Description: The "Awareness" page exhibits significant layout issues, with various content elements overlapping each other, making the page unreadable or visually unappealing. Furthermore, interactive elements or the page itself does not respond to user clicks, effectively rendering the page unusable.

Expected Behavior: The "Awareness" page should display content with a correct and clean layout, ensuring no elements overlap and all content is clearly visible and readable. All interactive elements within the page should respond correctly to user clicks, and the page should allow for proper navigation and interaction.

Actual Behavior: Upon navigating to the "Awareness" page, its layout is visually incorrect due to overlapping elements. Additionally, clicking anywhere on the page does not trigger any response, and the user remains stuck on the homepage, unable to access the Awareness content or functionality.

Steps to Reproduce:

Navigate to the "Awareness" page 

Observe the page layout for any overlapping content or elements.

Attempt to click on various parts of the page, including any supposed interactive elements.

Observe that the page does not respond to clicks, and the user remains on the homepage.

Environment:

OS: Windows 11

Browser/Device: Chrome 120, Samsung A22

App Version: v2.5.0

Test Data: User: user@cleancity.com / Password: password123

---

4.11. Defect ID: BUG011
Defect Title: Register Tabs are not highlighting

Description: When the user navigates to the "Register" page, the corresponding "Register" navigation tab or button in the application's header/menu does not visually highlight to indicate that it is the currently active page. Instead, the "Home" button/tab remains highlighted, leading to user confusion about their current location within the application.

Expected Behavior: When the user is on the "Register" page, the "Register" navigation tab/button should be visually highlighted to clearly indicate that it is the active page.

Actual Behavior: Upon navigating to the "Registration" page, the "Register" navigation element does not highlight. Instead, the "Home" button/tab continues to display as highlighted, providing incorrect visual feedback to the user.

Steps to Reproduce:

Navigate to the application's homepage.

Click on the "Register" link or button in the navigation menu.

Observe the navigation bar/menu; the "Register" tab is not highlighted, while the "Home" tab remains highlighted.

Environment:

OS: Windows 11

Browser/Device: Chrome 120, Samsung A22

App Version: v2.5.0

Test Data: User: user@cleancity.com / Password: password123
