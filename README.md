# OWASP Juice Shop Functionality and Vulnerability Assessment

## Project Overview

This project focuses on exploring the functionality of OWASP Juice Shop and performing a basic security assessment using Burp Suite Community Edition.

OWASP Juice Shop is an intentionally vulnerable web application used for learning web application security and understanding common security weaknesses.

The application was run locally, and HTTP requests and responses were captured and inspected using Burp Suite.

## Objectives

- Explore the main functionalities of the application.
- Understand HTTP requests and responses.
- Test authentication and session behavior.
- Evaluate input validation in product search.
- Test cart quantity validation and business logic.
- Document observations and potential security weaknesses.
- Suggest suitable remediation measures.

## Tools and Technologies

- OWASP Juice Shop
- Burp Suite Community Edition
- Node.js

## Software and Setup

### Tools Used

- **OWASP Juice Shop:** Intentionally vulnerable web application used for security testing.
- **Node.js:** JavaScript runtime used to run the application.
- **Burp Suite Community Edition:** Used to intercept and inspect HTTP requests and responses.
- **Web Browser:** Used to interact with the application.

### Official Downloads and Documentation

- Juice Shop GitHub repository: https://github.com/juice-shop/juice-shop/releases/tag/v20.3.0
- Node.js - Windows 64-bit Installer: https://nodejs.org/dist/v24.22.1/node-v24.22.1-x64.msi
- Burp Suite Community Edition: https://portswigger.net/burp/downloads

### Basic Setup

1. Install Node.js from the official website.
2. Obtain OWASP Juice Shop using the official project instructions.
3. Start Juice Shop locally and open it in a web browser.
4. Launch Burp Suite Community Edition.
5. Configure the browser to use Burp Suite's proxy, or use Burp's built-in browser.
6. Capture and inspect application requests.
7. Perform the documented tests in the authorized local environment.

### Test Environment

- Application: OWASP Juice Shop
- Hosting: Local machine
- Security testing tool: Burp Suite Community Edition
- Testing approach: HTTP request and response inspection

## Testing Methodology

1. Run OWASP Juice Shop locally.
2. Browse the application and identify its main functionalities.
3. Capture HTTP traffic using Burp Suite.
4. Inspect requests and responses in HTTP history.
5. Send relevant requests to Repeater for controlled testing.
6. Modify selected inputs and observe the responses.
7. Record test results and supporting screenshots.
8. Document findings, possible impacts, and recommendations.

## Test Categories

- Authentication and session testing
- Product search input validation
- Long input handling
- Cart quantity validation
- General functionality testing

## Key Observations

- The product search endpoint returned an HTTP 500 error for a specially crafted search input and exposed database error details.
- A long search input returned an HTTP 200 response with an empty result set.
- An unauthenticated account-information request returned an empty user object in the observed test.
- The cart quantity tests showed that zero was handled safely, negative quantity was not rejected, and alphanumeric quantity was rejected.

These observations are documented in the findings and test-results files. The impact and severity of potential weaknesses must be evaluated using the actual application behavior and supporting evidence.


## Conclusion

This assessment provided practical experience in web application functionality testing, HTTP traffic analysis, input validation testing, and business logic testing. The observations demonstrate the importance of proper input handling, secure error responses, authentication checks, and server-side validation.

## Disclaimer

This assessment was conducted on a locally hosted OWASP Juice Shop instance for educational purposes. Testing was limited to the authorized lab environment.

## Final Project Report

The complete project report contains the methodology, functionality testing, security findings, Burp Suite screenshots, observations, and recommendations.

**[View Final Report (PDF)](OWASP_Juice_Shop_Final_Report.pdf)**
