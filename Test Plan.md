<h1 id="Test-plan">Test plan for ITFlow exploratory testing.</h1>

### Description:
This project aims to verify the functionality and UX of the [ITFlow](https://itflow.org/) website through a combination of exploratory and manual testing. The main focus of the tests includes core user functionalities like login, registration, admin panel, ticketing, and billing. Testing will be conducted on a Windows 11 desktop machine using Google Chrome, Brave, and Edge to ensure compatibility across different browsers. Additionally, basic checks for security vulnerabilities and accessibility compliance will be included to assess overall user experience and system robustness.

### Scope of testing:

- **Functional testing**:
  * Verify core functionalities such as login, registration, admin panel access, ticketing, billing, client management, and data management.
  * Ensure accurate data processing.
  * Test various input combinations and edge cases.
  * Validate error handling and feedback messages.

- **Usability testing**:
  * Evaluate the user interface design.
  * Assess the ease of navigation and workflow.
  * Identify any usability issues.
    
- **Compatibility testing**:
  * Ensure compatibility with different browsers, operating systems, and devices.
  * Test responsiveness on various screen sizes and resolutions.
    
- **Security testing**:
  * Identify and address potential security vulnerabilities.
  * Test authentication and authorization mechanisms.

### Testing environment:

- **Operating system**: Windows 11 (Desktop machine)
- **Browser**: Google Chrome, Brave, Edge 
  

### Test schedule:
* **Start date**: 14.09.2025
* **End date**: 30.09.2025 

### Resources:

- **Manual tester**: Responsible for exploratory testing and creating test data.
- **Tools**: 
   * DevTools
   * ShareX and ScreenPal
   * BugMagnet

### Entry criteria:
- Smoke tests are performed and the code is stable for testing.
- Test environment is set up and ready.
- Test plan is reviewed, and approved.
- Test data are designed.
  
  

### Exit criteria:

- All tests from the check list are executed.
- All critical and major defects should be fixed or have a solution plan.
- Test coverage should be at least 80%.
- Test summary report is ready.

### Risks and mitigations:
- **Risk**: Changes in requirements or specifications during testing.
  - **Mitigation**: Maintain constant contact with the product owner and monitor documentation changes.
- **Risk**: Lack of testers knowledge.
  - **Mitigation**: Ensure proper training and development to improve testing skills of team members.
- **Risk**: Delays in test execution.
  - **Mitigation**:  Prioritize critical test cases and conduct proper time estimation to avoid delays.

<h1 id="Test-Check">Test checklist.</h1>

**Functional**:

- Verify user login functionality.
- Test user registration process.
- Ensure proper logging and error reporting mechanisms.
- Verify password reset and recovery processes.
- Check admin panel access and functionalities.
- Verify user logout functionality.
- Validate error handling and feedback messages for incorrect inputs. 
- Validate ticket creation, updating, and closing.
- Test billing module for invoice generation and payment processing.
- Verify client management features (add, edit, delete clients).
- Test user profile management (update personal information, change password).
- Ensure data management functionalities (import/export data).
- Test various input combinations and edge cases for all forms.
- Check session management (login timeout, session persistence).
- Validate email notifications and alerts.
- Test search functionality across different modules.
- Verify file upload and download features.
- Check sorting in data tables.
- Check for any broken links or missing resources.

**Usability testing**:

- Evaluate the overall user interface design for consistency.
- Assess the visual appeal and readability of the interface.
- Assess the ease of navigation across different sections.
- Evaluate the responsiveness of the UI to user actions.
- Check RWD for different screen sizes and resolutions.
- Test the intuitiveness of the workflows.
- Check the clarity and helpfulness of on-screen instructions and tooltips.
- Test the application’s behavior with different input methods (mouse, keyboard, touch).
- Check for any distracting elements or unnecessary animations.
- Test the application’s onboarding process for new users.
- Evaluate the application’s help and support features (FAQs, contact support).

 **Accessibility**:
 - Test screen reader compatibility.
 - Test voice commands for navigation and interaction
 - Avoid using color as the sole method of conveying information.
 - Check if objects are cleary
 - Check transcripts, or audio descriptions for all sound and video content.
 - Ensure that all form fields have associated labels.

 **Security**:
 
 - Ensure all user inputs are validated on both client and server sides.
 - Ensure proper permission checks for all sensitive actions.
 - Check session timeout and inactivity logout.
 - Chek proper data encyption.
 - Ensure no sensitive information is exposed in error messages.
 - Test strong password policies (minimum length, complexity requirements).
 
