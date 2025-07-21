🧪 CleanCity QA Final Test Report
---
📋 Project Summary

Application Name: CleanCity – Waste Pickup Scheduler<br>

Testing Period: July 10 – July 21, 2025 <br>

Tested By: Antony Manyenze, Susan Ng'ang'a, Teresiah Waweru

**Objective:**

Ensure functional integrity, usability, accessibility, and performance of the CleanCity web application, including registration, scheduling, administrative functions, content management, Authentication system, community features, dashboard interaction, and navigation flows.

### ✅ Test Coverage Overview
| Feature              | Status | Functional Req. | Notes                                             |
| -------------------- | ------ | -------------- | ------------------------------------------------- |
| Home Page Load       | ✅ Pass | FR-01       | Loaded correctly via React script.                |
| User Registration    | ✅ Pass | FR-02          | Valid credentials used.                           |
| Schedule Pickup Form | ✅ Pass | FR-03          | Dropdowns, text fields, and submit button tested. |
| Login                | ✅ Pass | FR-04          | Credentials verified after registration.          |
| Dashboard Navigation | ✅ Pass | FR-05          | Reached successfully post-login.                  |
| Blog Access         | ✅ Pass | FR-06          | Navigation functional.                            |
| Community Page      | ✅ Pass | FR-07          | Navigation functional.                            |
| Awareness Page      | ✅ Pass | FR-08          | Navigation functional.                            |
| Feedback Page       | ✅ Pass | FR-09          | Navigation functional.                            |
| Logout Functionality | ✅ Pass | FR-10          | Session terminated and returned to login page.    |
| Admin pickup request modification| Fail | FR-055 | There is no user interface available to modify requests|


---
🧪 Automated Testing with Jest & Lighthouse
---
Tools Used: Jest, React Testing Library, Lighthouse, Visual Studio Code, Git, GitHub

Jest Component & Integration Tests
Test Script Path: src/__tests__/cleancity.test.js

Description:

Utilizes Jest and React Testing Library to render components and simulate user interactions.

Tests core user flows including registration, pickup scheduling, login, and page navigation.

Verifies component rendering, state updates, and successful data submission (mocked API calls for external interactions).

Focuses on unit and integration level testing for fast feedback during development.


Execution Result:

All Jest tests passed successfully with rapid execution times.

Confirmed component-level functional integrity across key features.
---

Lighthouse Performance & Accessibility Audit

Audit Scope: Homepage, Login Page, Dashboard, Awareness Page (mobile simulation)


Description:

Lighthouse was used to audit key pages for performance, accessibility, best practices, and SEO.

Audits were run simulating mobile network conditions to identify real-world user experience issues.


Audit Results Summary:

Performance: Overall score was moderate. Noted slow image loading on the "Awareness Page" and a slight delay in form response, particularly on simulated mobile networks, indicating potential optimization needs for asset delivery and initial render.

Accessibility: Identified some areas for improvement, particularly regarding keyboard accessibility for notification pop-ups and sufficient color contrast on certain UI elements.


Best Practices & SEO: Generally good scores, indicating adherence to modern web standards.

---

📂 Defect Log Summary
Defect ID: D-001
Title: Inconsistent App URL Handling

Description:
Opening the application using VS Code Live Server (http://127.0.0.1:5500) results in data loss — scheduled pickups do not reflect in the dashboard. However, launching via React script (http://localhost:3000) performs as expected. This suggests an environment or proxy configuration issue rather than a core application bug.

Screenshots:
📎 Tests/Jira_Screenshots/Screenshot.png (Live Server)
📎 Tests/Jira_Screenshots/Screenshot.png (React App)

Severity: Critical
Priority: High
Status: Open
Logged By: Antony Manyenze
Date: July 21, 2025

---
🔚 Final Notes
Jest tests confirm the functional readiness of individual components and integrated flows.

Lighthouse audit provides valuable insights into performance bottlenecks (especially image loading) and accessibility gaps, which are crucial for user experience.

The URL handling defect (D-001) is confirmed to be environment-specific, not a core application logic issue.

The core functionality is largely working as intended when run in the correct environment, but performance and accessibility improvements are recommended for a production-ready system.

✅ This test cycle confirms functional readiness of CleanCity for presentation, with clear areas for further optimization identified through Lighthouse.

Prepared by: Antony Manyenze
Date: July 21, 2025
