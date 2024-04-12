# Overall Test Plan

In general, our testing strategy is to first assess each component of each screen. We will then assess each screen and how each component on the screen interacts with each other. For both cases, there will be 2 different tests. In some situations, this will involve creating test data or inputs that will then be confirmed to appear and function correctly. In other cases, the functionality and appearance may not be dynamic between users, so the test results will be concrete, and we will always be looking for the same result.

---

## Test Case Descriptions

### Web Admin Test 1

- **Objective:** To verify that the user can authenticate with Spotify when opening the app.
- **Procedure:** This will be tested by clicking on the login button on the first screen of the app. The user’s Spotify information will be inputted.
- **Output:** The user is presented with a Spotify login screen and will be allowed to authenticate and move onto the next screen of the app.
- **Case Indication:** Normal
- **Test Indications:** Whitebox, Functional, Integration

### Web Admin Test 2

- **Objective:** Verifying that posts load correctly when looking at the feed portion of the app.
- **Procedure:** The feed will be prepopulated with posts. Then, this test will have a different user login, navigate to the feed page, and examine the contents of the display.
- **Inputs:** Prepopulated posts sent to the feed.
- **Outputs:** Posts displayed on the feed to users.
- **Case Indication:** Normal
- **Test Indications:** Blackbox, Functional, Unit

### Web Admin Test 3

- **Objective:** To test the user’s ability to create a post.
- **Procedure:** This test will involve a user typing and submitting messages in the feed portion of the app. After entering the message, the user will click post.
- **Inputs:** Various messages to verify that strings of each type of acceptable formatting (numbers, letters, uppercase, lowercase, punctuation) are accounted for.
- **Outputs:** The text box for user input will be cleared and the message typed will be displayed in the feed portion of the page along with the user’s profile name.
- **Case Indication:** Normal
- **Test Indications:** Blackbox, Functional, Unit tests

### Web Admin Test 4

- **Objective:** To test that the user’s profile information correctly appears on their profile page.
- **Procedure:** This will be tested by navigating to the profile page and looking for specific indicators that should show up. Pre-created posts will be created on the profile so that it can be viewed.
- **Outputs:** Each of the created posts and user information is correctly displayed on the page and interactable.
- **Case Indication:** Normal
- **Test Indications:** Whitebox, Functional, Integration

### Server Test 1

- **Objective:** To test the Database server connection.
- **Procedure:** The database server is hosted in the cloud and spins up when needed. This test will determine if the backend connects to it properly.
- **Input:** The input will come from the backend running and sending a connection request to the azure database.
- **Outputs:** The server will spin up if currently offline and database queries from the backend will work as intended. And spun up in a timely manner.
- **Case Indication:** Normal
- **Test Indications:** Whitebox, Performance, Integration

### Networking Test 1

- **Objective:** This test will ensure that the front-end and back-end can communicate correctly over the network.
- **Procedure:** This test will run certain HTTP requests from the front-end and expect the back end to properly route, operate, and return the expected results to the front-end.
- **Input:** The front-end will generate HTTP requests of varying types with varying payloads.
- **Output:** The back end will return the correct information to the front-end.
- **Case Indication:** Both
- **Test Indications:** Whitebox, Functional, Integration

### Networking Test 2

- **Objective:** This test will ensure that the back end can communicate with the Spotify API correctly.
- **Procedure:** The test will run certain API requests to the Spotify API and expect the correct information to be returned to it.
- **Input:** The back end will generate payloads to send to the Spotify API.
- **Output:** The correct information is received by the backend via the response.
- **Case Indication:** Both
- **Test Indications:** Whitebox, Functional, Integration

### Networking Test 3

- **Objective:** Validate the interaction between our front-end system and the Spotify API.
- **Procedure:** Assess functionality and reliability of communication between frontend and Spotify API.
- **Inputs:** Loading in Spotify data through the frontend.
- **Outputs:** Frontend is successfully able to fetch and display Spotify data on the UI.
- **Case Indication:** Normal
- **Test Indications:** Whitebox, Functional, Integration

### Web Admin Test 5

- **Objective:** Verify the system’s response when the login page is skipped, assuming the user is already logged in.
- **Procedure:** Attempt to access the login page when the user is already logged in to assess the system’s behavior.
- **Inputs:** Attempt to reach the login page URL without logging out.
- **Outputs:** The system understanding the user is already logged in and redirects them to the appropriate section, skipping the login page.
- **Case Indication:** Normal
- **Test Indications:** Whitebox, Functional, Integration

### Full System Test

- **Objective:** This test ensures that the system will be working together properly.
- **Procedure:** We will deploy this agent on a server that will be configured to monitor a specific log file.
- **Inputs:** Log File.
- **Outputs:** Appropriate database queries based on the data from the log file.
- **Case Indication:** Normal
- **Test Indications:** Whitebox, Functional, Integration

---


| Identifier | Normal/Abnormal/Boundry | Blackbox/Whitebox | Functional/Performance | Unit/Integration |
| ------ | ------ | ------ | ------ | ------ |
| WA1 | Normal | Whitebox | Functional | Integration |
| WA2 | Normal | Blackbox | Functional | Unit Test |
| WA3 | Normal | Blackbox | Functional | Unit Test |
| WA4 | Normal | Whitebox | Functional | Integration |
| WA5 | Normal | Whitebox | Functional | Integration |
| ST1 | Normal | Whitebox | Performance | Integration |
| NT1 | Both | Whitebox | Functional | Integration |
| NT2 | Both | Whitebox | Functional | Integration |
| NT3 | Normal | Whitebox | Functional | Integration |
| FST | Normal | Whitebox | Functional | Integration |
