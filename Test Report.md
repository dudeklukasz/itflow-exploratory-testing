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



<h2 id="Bug-Reports">1. User can add new vendor with empty name (spacebar).</h2>

**Description**: A user is able to create a new vendor with only a spacebar as the name, bypassing the required field validation.

**Preconditions**: User is logged in with active account.

**Steps to reproduce**:
- Navigate to the vendor management section.
- Click the "Add New Vendor" button.
- Enter a spacebar in the vendor name field.
- Leave other required fields blank.
- Click the "Create" button.

**Expected result**: The system should display an error message indicating that the vendor name is required and cannot be empty. The user should not be able to proceed with the vendor creation process.

**Actual result**: The user is allowed to create the vendor with an empty name, potentially leading to data inconsistencies and errors in subsequent operations.

**Priority**: Medium

**Browser compatibility**: This issue has been observed in all tested browsers: Google Chrome, Brave, and Edge.



https://github.com/user-attachments/assets/2c220259-be9a-4574-a202-80f3410935c6



<h2 id="Bug-Reports">2. Importing new client without providing any files leads to HTTP error 500.</h2>

**Description**: When attempting to import a new client without providing any associated files, the system returns an HTTP Error 500. 

**Preconditions**: User is logged in with active account.

**Steps to reproduce**:
- Navigate to the client section.
- On the "Add New" click dropdown arrow and select "Import"
- Without adding any files click "Import" button

**Expected result**: The system should display an error message indicating that at least one file is required for client import. The user should not be able to proceed with the import process.

**Actual result**: An HTTP error 500 is returned.

**Priority**: Medium

**Browser compatibility**: This issue has been observed in all tested browsers: Google Chrome, Brave, and Edge.



https://github.com/user-attachments/assets/99282403-6adc-4e24-a78a-7f5a06432f1f

<h2 id="Bug-Reports">3. Missing length validation for desciption input when creating or editing vendors.</h2>

**Description**: There is no validation in place for the description field length when creating or editing vendors. Entering a description with more than 200 characters cause the user interface (UI) to break, and entering more than 300 characters lead to an HTTP 500 error.

**Preconditions**: User is logged in with active account.

**Steps to reproduce**:
- Navigate to the vendor section.
- Click "Add new vendor" or eddit existing one.
- Enter a description with more than 200 or 300 characters.
- Click "Confirm" button.
- Observe the system's response.

**Expected result**: The system should validate the description field length and provide a warning or limit the input to appropriate length.

**Actual result**: Depending on length input system UI breaks or an HTTP error 500 is returned.

**Priority**: Medium

**Browser compatibility**: This issue has been observed in all tested browsers: Google Chrome, Brave, and Edge.



https://github.com/user-attachments/assets/8f3add4c-cdfc-4071-b782-37f89ffe60d2

<h2 id="Bug-Reports">4. Missing file type validation for user avatar.</h2>

**Description**: The system lacks validation for the file type when uploading an avatar for a new user. Uploading a non-image file format (e.g., .txt, .pdf) results in an HTTP 500 error.

**Preconditions**: User is logged in as an administrator.

**Steps to reproduce**:
- Navigate to the admin panel.
- Open the "Users" tab.
- Click the "Add New User" button.
- Fill in all required fields for the new user.
- Upload a non-image file (e.g., a .txt file) as the avatar.
- Click the "Create" button.
- Observe the system's response.

**Expected result**: The system should display an error message indicating that only image files are allowed for user avatars. The user should not be able to proceed with the creation of the new user.

**Actual result**: An HTTP 500 error is returned, indicating a server-side issue likely caused by attempting to process a non-image file as an avatar.

**Priority**: Medium

**Browser compatibility**: This issue has been observed in all tested browsers: Google Chrome, Brave, and Edge.



https://github.com/user-attachments/assets/976633a0-2870-41be-ac79-7b370cfefea0

<h2 id="Bug-Reports">5. User can create tasks with negative time.</h2>

**Description**: The system allows users to create tasks with negative time estimates, leading to inaccurate overall time estimates for tickets. This can result in significant errors in job planning and scheduling.

**Preconditions**: User is logged in with active account.

**Steps to reproduce**:
- Navigate to the tickets section.
- Select an existing ticket.
- Add a new task.
- Enter a negative value for the estimated time.
- Save the task.
- Observe the system's response.

**Expected result**: The system should prevent the creation of tasks with negative time estimates and display an error message indicating that the time value must be positive.

**Actual result**: The task is created with a negative time estimate. This negative value is incorrectly added to the overall ticket time estimate, leading to inaccurate calculations.

**Priority**: Medium

**Browser compatibility**: This issue has been observed in all tested browsers: Google Chrome, Brave, and Edge.




https://github.com/user-attachments/assets/f67f2022-e552-494f-a9c2-642245c2bb6b


<h2 id="Bug-Reports">6. Admin can view password by clicking padlock icon.</h2>

**Description**: The admin panel allows to view sensitive user passwords by clicking on a padlock icon, which is an unexpected behavior. This could potentially lead to security breaches.

**Preconditions**: User is logged in as an administrator.

**Steps to reproduce**:
- Navigate to the admin panel.
- Go to the "Users" tab.
- Click on the "Create New User" button.
- Fill in the password field.
- Click on the padlock icon.
- Observe the password innput.

**Expected result**: The padlock icon should be purely decorative and not have any interactive functionality. Clicking on it should not reveal the password.
**Actual result**: Clicking on the padlock icon reveals the password, potentially compromising sensitive information.

**Priority**: Medium

**Browser compatibility**: This issue has been observed in all tested browsers: Google Chrome, Brave, and Edge.



https://github.com/user-attachments/assets/844c00d6-f84e-4dcd-9639-3f1b93d7bcf4

<h2 id="Bug-Reports">7. Missing option to directly add assets when creating new recurring ticket.</h2>

**Description**: When creating a new recurring ticket, there is no direct option to add assets immediately. Users have to create the ticket first and then go back to edit it to add assets.

**Preconditions**: User is logged in with active account.

**Steps to reproduce**:
- Navigate to the recurring ticket section.
- Click the "Add New Recurring Ticket" button.
- Enter a spacebar in the vendor name field.
- Fill in the required fields.
- Select "Assets" tab.
  

**Expected result**: There should be an option to add assets directly when creating the recurring ticket, just like there is one in edit options.

**Actual result**: Assets tab have blank white space with missing dropdown menu.

**Priority**: Medium

**Browser compatibility**: This issue has been observed in all tested browsers: Google Chrome, Brave, and Edge.



https://github.com/user-attachments/assets/f9a05b53-9f9c-4663-96f3-8e1b26591df0


<h2 id="Bug-Reports">8. Duplicate file upload in documents section leads to 500 error.</h2>

**Description**: The system allows users to upload the same file multiple times to a document, leading to an HTTP 500 error upon saving the document. 

**Preconditions**: User is logged in with active account.
A client and document are created.

**Steps to reproduce**:
- Navigate to the "Clients" tab.
- Select a client.
- Navigate to the "Documents" tab.
- Click the "+" button to add a file.
- Upload a file of your choice.
- Click the "+" button again and select the same file.
- Save the document.


**Expected result**: File should be removed from the list after adding it, same as it works with other lists.
**Actual result**: The system allows the user to add the same file multiple times. When the document is saved, an HTTP 500 error occurs.

**Priority**: Medium

**Browser compatibility**: This issue has been observed in all tested browsers: Google Chrome, Brave, and Edge.



https://github.com/user-attachments/assets/19027ed0-d7b0-4817-9542-2df0dee168f1

<h2 id="Bug-Reports">9. Admin can't log out.</h2>

**Description**: When an admin attempts to log out of the application they are redirected to an empty page. It is possible to navigate back to the previous page using the browser's back button.

**Steps to reproduce**:
- Navigate to the admin login page.
- Enter correct credentials and log in.
- Open the right-top panel and click on the "Logout" button.

**Expected result**: The user should be successfully logged out and redirected to the login page or a designated logout page.

**Actual result**: The user is redirected to an empty page and can navigate back to the previous page using the browser's back button.

**Priority**: High

**Browser compatibility**: This issue has been observed in all tested browsers: Google Chrome, Brave, and Edge.



https://github.com/user-attachments/assets/037200f0-a291-4752-a02a-b71eb6eec7bc


<h2 id="Bug-Reports">10. Incorrect currency conversion for cross-currency transfers.</h2>

**Description**: The system allows users to initiate transfers between accounts with different currencies without performing accurate currency conversion. This can lead to significant financial discrepancies and potential losses for users.

**Preconditions**: User is logged in with active account.
Two accounts with different currencies.

**Steps to reproduce**:
- Navigate to the "Transfers" tab.
- Click the "New Transfer" button.
- Select the source account with one currency.
- Select the destination account with a different currency.
- Enter the desired transfer amount.
- Initiate the transfer.


**Expected result**: The system should either:
- Prevent the transfer and display an error message indicating that currency conversion is not supported.
- Automatically convert the transfer amount to the destination currency's equivalent value using a real-time exchange rate.
  
**Actual result**: The system allows the transfer to proceed without performing any currency conversion. This can result in significant financial losses for the user, as the actual transferred amount may be significantly different from the intended amount.

**Priority**: High

**Browser compatibility**: This issue has been observed in all tested browsers: Google Chrome, Brave, and Edge.




https://github.com/user-attachments/assets/4475508f-00cd-47c6-8b8f-fcea362c94d7










