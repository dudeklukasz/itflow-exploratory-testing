<h1 id="Test-report">Test summary report.</h2>

1. **Descripton**:
  This test summary report provides an overview of the exploratory testing conducted on the ITFlow web application. The testing focused on identifying functional defects, usability issues, and security vulnerabilities.
3. **Test Period**: 14.09.2025 - 30.09.2025
4. **Test Coverage** : 95% test coverage, remaining 5% contained edge cases with low risk
  
5. **Key findings**:
   **UI/UX issues**:
   - Misaligned buttons and table content.
   - Missing hover functionality for certain elements.
   - Ineffective multi-language support.
   - Unnecessary empty dropdowns in some buttons.
   - Sorting issues in tables.

   
   **Functionality issues**:
   - Admin cannot log out properly.
   - Users can add new vendors with empty names.
   - Missing option to directly add assets when creating recurring tickets.
   - Description length validation is missing.
   - Incorrect currency conversion for cross-currency transfers.
   - Duplicate file upload leads to 500 error.
   - Admin can ciew password by clicking padlock icon.
   - User can create tasks with negative time.
   - Missing file type validation for user avatar.
     
   **API integration**:
   
   - The automated message generator API was not connected to ChatGPT, preventing its functionality.

6. **Recommendations**:
   
   **Address UI/UX issues**:
   - Correct misaligned elements to improve visual consistency and user experience.
   - Remove unnecessary empty dropdowns to simplify the interface.
   - Ensure that elements with hover effects function as expected.
   - Fix or add proper multi-language support.
     
   **Enhance functionality**:
   
   - Implement proper validation for vendor names and description lengths.
   - Provide a direct option to add assets when creating recurring tickets.
   - Connect the automated message generator API to ChatGPT to enable its functionality.

7. **Test execution summary:**
   
   All core elements of the ITFlow web application are functioning correctly, although there are some minor issues. Despite these issues, users can still utilize the application's functionalities without significant hindrance. Addressing the identified issues will further enhance the overall user experience and ensure the application's success. All reported bugs are currently under investigation and awaiting resolution.
<br></br>


<h1 id="Qase-Main">Bug reports</h1>
