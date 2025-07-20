#DEFECTS
---
Title:"Edit" button in Admin Panel's Actions column is unresponsive.

Jira/GitHub (Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-43

Requirement affected:This prevents administrators from modifying any data or settings for the corresponding items, severely impacting administrative control and data management.

Severity:Critical

Summary:On various administrative management pages, the "Edit" button located within the "Actions" column for individual entries is completely unresponsive when clicked.

---
Title: Admin filter combines incorrectly: Status filter is ignored when Location filter is applied simultaneously.

Jira/Github (Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-42

Requirement affected:As a result, all requests from the specified location are displayed, regardless of their status, effectively ignoring the chosen status filter. This leads to inaccurate data presentation and hinders administrative efficiency.

Severity:Major

Summary:When an administrator attempts to filter pickup requests by both a specific Status (e.g., "Pending") and a specific Location (e.g., "Eldoret") on the "Manage Requests" page, the system incorrectly prioritizes or exclusively applies the Location filter. 

---
Title:"Contact Us" form submits successfully without internet connection (data loss)

Jira/Github(Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-41

Requirements affected:The "Contact Us" form incorrectly indicates a successful submission even when the device has no internet connection

Severity:Major

Summary: leading to user data loss as the message never reaches the server.

---
Title:User password change allows current password as new password.

Jira/Github(Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-40

Requirements affected:The "Change Password" feature allows users to set their new password to be identical to their current password without any validation

Severity:Minor

Summary: This leads to a redundant and potentially confusing action.

---
Title:UI elements flicker briefly when navigating between authenticated pages.

Jira/Github(Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-39

Requirements affected:When a logged-in user navigates between different internal pages, there's a brief, noticeable flicker of UI elements

Severity:Cosmetic

Summary:This suggests incomplete page loading or rendering issues.

---
Title:Awareness Page" images load slowly on mobile networks

Jira/Github(Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-38

Requirements affected:The performance issue specifically impacts the loading of images and multimedia on this particular page.

Severity:Major

Summary:Images and multimedia content on the "Awareness Page" take an excessive amount of time to load when viewed on a simulated slow mobile network connection

---
Title:User cannot schedule a pickup for dates far in the future

Jira/Github(Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-37

Requirements affected:The date picker for scheduling a pickup request is limited to a relatively short future range.

Severity:Minor

Summary: This prevents users from scheduling pickups for dates far in advance.

---
Title:Notification pop-up are not keyboard accessible.

Jira/Github(Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-36

Requirements affected:This affects the usability and accessibility of the application wherever these specific notification pop-ups are displayed

Severity:Minor

Summary:Success or error notification pop-ups, while visible, cannot be navigated to or dismissed using only keyboard controls

---
Title:Admin login page allows brute-force attacks due to lack of lockout mechanism.

Jira/Github(Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-35

Requirements affected:The entire integrity, confidentiality, and availability of the system, its data, and its users, all stemming from the vulnerability of the administrative login process.

Severity:Critical

Summary: An attacker can make an unlimited number of failed login attempts without any delay or account lockout, making it vulnerable to brute-force attacks

---
Title:Password field accepts special characters not allowed during registration.

Jira/Github(Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-34

Requirements affected:The core issue lies within the input validation and character handling for the password field during the user registration process, which has cascading effects on user authentication, data integrity, and potential security posture of the application.

Severity:Major

Summary:The registration form's password field allows users to include certain special characters that are then not correctly processed upon login, leading to authentication failure.

---

Title:After registration page does not automatically log in.

Jira/Github(Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-33

Requirements affected:The primary affected areas are the Registration and User Authentication modules, specifically the post-registration workflow and session management.

Severity:Critical

Summary:Upon successful completion of the user registration process, the CleanCity application displays a "Registration Successful" message. However, the system fails to automatically log in the newly created user or redirect them to their personalized dashboard or the application's home page

---

Title:Logging out leads you to the request pickup page.

Jira/Github(Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-32

Requirements affected:The most directly affected areas are the logout process itself, the application's routing mechanism, and potentially the session management.

Severity:Medium

Summary:This behavior is contrary to standard web application logout practices and presents a potential security or usability concern. The "Request Pickup" page is typically intended for logged-in users, and displaying it after logout may imply that the session has not been fully terminated or could expose sensitive information if not handled correctly.

---
Title:New Registered users do not reflect on system dashboard.

Jira/Github(Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-31

Requirements affected:The core problem is a disconnect between the successful registration of a new user and the dashboard's ability to accurately retrieve and display that new user's information.

Severity:Critical

Summary:This includes basic profile details like username or email, and any user-specific data that would typically populate a personalized dashboard. The dashboard appears blank or generic, failing to reflect the logged-in user's data. This prevents users from accessing their own account-related information and functionalities immediately after joining and logging in

---
Title:Misleading error message when attempting to register with an already registered email.

Jira/Github(Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-30

Requirements affected:This directly impacts the system's ability to communicate effectively with its users during a critical interaction (registration), hindering their ability to successfully complete the process.

Severity:Minor

Summary:When a user attempts to register with an email address that is already associated with an existing account, the error message provided is generic  instead of specific ("Email already registered") 

---
Title:Login Here button on the home page does not respond.

Jira/Github(Bug) Link:https://zetech-team.atlassian.net/browse/CLEANCITY-29

Requirements affected:This directly impacts the fundamental ability of the user to initiate the login process, which is a core functional requirement.

Severity:Critical

Summary:On the CleanCity application's home page, the "Login Here" button, intended to redirect users to the login screen, is completely unresponsive when clicked. This prevents users from accessing the login functionality and subsequently, the application itself.
