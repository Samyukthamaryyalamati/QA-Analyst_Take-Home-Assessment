# Manual Test Cases For Linq Visitor Flow

## Positive Scenarios
**Test Case ID**: PS001
**Description**: Save contact with all valid fields
**Steps**:
1. Navigate to "https://linqapp.com/welcome"
2.  a.If you're a new member,Sign Up using any method: Phone Number/ Email/ Apple Account/Google Account/ LinkedIn Account
    b.If you're an existing member, Login using Phone Number/ Email/ Apple Account/ Google Account/ LinkedIn Account.
3. Once logged in,  Click on "Contacts" on the left-hand side of the page.
4. Click on "Add Person" icon located at the bottom of the page.
5. Fill all the required field - "First & Last Name" , "Phone Number" , "Email" , "Job Title" , "Organization / Company" , "Location".
6. Click the "Save Changes" button on the bottom of the form.
**Expected Results**: Contact is saved successfully and a confirmation pop-up is displayed at the bottom of the screen.
**Actual Output**: Contact saved successfully and received confirmation pop-up on the screen.

**Test Case ID**: PS002
**Description**: Save contact with special characters in the name field.
**Steps**:
1. Navigate to "https://linqapp.com/welcome"
2.  a.If you're a new member,Sign Up using any method: Phone Number/ Email/ Apple Account/Google Account/ LinkedIn Account
    b.If you're an existing member, Login using Phone Number/ Email/ Apple Account/ Google Account/ LinkedIn Account.
3. Once logged in,  Click on "Contacts" on the left-hand side of the page.
4. Click on "Add Person" icon located at the bottom of the page.
5. In the "First & Last Name" field, enter special characters (e.g. "@#Sam!!91")
6. Fill in the remaining field with valid data - "Phone Number" , "Email" , "Job Title" , "Organization / Company" , "Location".
7. Click the "Save Changes" button on the bottom of the form.
**Expected Results**:
- If special Charecters are allowed: The contact should be saved successfully with the entered name.
- If special characters are not allowed: A validation error message should appear.
**Actual Output**: Contact saved successfully with the special charecters in the name filed and received confirmation pop-up on the screen.

## Negative Senarios
**Test Case ID**: NS001
**Description**: Save contact with all fields empty
**Steps**:
1. Navigate to "https://linqapp.com/welcome"
2.  a.If you're a new member,Sign Up using any method: Phone Number/ Email/ Apple Account/Google Account/ LinkedIn Account
    b.If you're an existing member, Login using Phone Number/ Email/ Apple Account/ Google Account/ LinkedIn Account.
3. Once logged in,  Click on "Contacts" on the left-hand side of the page.
4. Click on "Add Person" icon located at the bottom of the page.
5. Do not fill any of the field (leave everything empty)
6. Click the "Save Changes" button on the bottom of the form.
**Expected Results**: Validation error messages should appear for each required field, and the form should not be submitted until all mandatory fields are filled.
**Actual Output**: Received error messages: "Please provde information in at least one of the field for this contact." successfully.

**Test Case ID**: NS002
**Description**: Save a duplicate contact with the same email address
**Steps**:
1. Navigate to "https://linqapp.com/welcome"
2.  a.If you're a new member,Sign Up using any method: Phone Number/ Email/ Apple Account/Google Account/ LinkedIn Account
    b.If you're an existing member, Login using Phone Number/ Email/ Apple Account/ Google Account/ LinkedIn Account.
3. Once logged in,  Click on "Contacts" on the left-hand side of the page.
4. Click on "Add Person" icon located at the bottom of the page.
5. Fill all the required field - "First & Last Name" , "Phone Number" , "Email" , "Job Title" , "Organization / Company" , "Location".
6. After successfully saving the contact, click "Add Person" icon again
7. Enter a new name but reuse the **Same email** .
8. Fill the rest of the field with valid data.
9. Click the "Save Changes" button on the bottom of the form.
**Expected Results**: An error or warning message should appear stating that a contact with this email already exists.
**Actual Output**: Successfully received a warning message: "A Contact with this email already exists."

**Test Case ID**: NS003
**Description**: Save a contact with the all required field filled but with no name(empty name filed)
**Steps**:
1. Navigate to "https://linqapp.com/welcome"
2.  a.If you're a new member,Sign Up using any method: Phone Number/ Email/ Apple Account/Google Account/ LinkedIn Account
    b.If you're an existing member, Login using Phone Number/ Email/ Apple Account/ Google Account/ LinkedIn Account.
3. Once logged in,  Click on "Contacts" on the left-hand side of the page.
4. Click on "Add Person" icon located at the bottom of the page.
5. Leave the **First & Last Name** field empty. 
6. Fill all the other required field - "Phone Number" , "Email" , "Job Title" , "Organization / Company" , "Location".
7. Click the "Save Changes" button on the bottom of the form.
**Expected Results**:
- If the name field is required: A validation error should appear indicating that the name field cannot be empty.
- If the name field is optional: The contact should be saved successfully with the other valid data.
**Actual Output**: Contact saved successfully and No error message was shown.

**Test Case ID**: NS004
**Description**: Save a contact with invalid characters in the email field
**Steps**:
1. Navigate to "https://linqapp.com/welcome"
2.  a.If you're a new member,Sign Up using any method: Phone Number/ Email/ Apple Account/Google Account/ LinkedIn Account
    b.If you're an existing member, Login using Phone Number/ Email/ Apple Account/ Google Account/ LinkedIn Account.
3. Once logged in,  Click on "Contacts" on the left-hand side of the page.
4. Click on "Add Person" icon located at the bottom of the page.
5. Fill all the required field - "First & Last Name", "Phone Number" , "Email" , "Job Title" , "Organization / Company" , "Location".
6. Fill the email field with invalid charecter (e.g. sam@@gmail.com / sam@.com)
7. Click the "Save Changes" button on the bottom of the form.
**Expected Results**: A validation error message should appear indicating that the email address format is invalid, and the contact should not be saved.
**Actual Output**: Successfully displaying an error message:"Please enter a valid email."

**Test Case ID**: NS005
**Description**: Save a contact with invalid phone number
**Steps**:
1. Navigate to "https://linqapp.com/welcome"
2.  a.If you're a new member,Sign Up using any method: Phone Number/ Email/ Apple Account/Google Account/ LinkedIn Account
    b.If you're an existing member, Login using Phone Number/ Email/ Apple Account/ Google Account/ LinkedIn Account.
3. Once logged in,  Click on "Contacts" on the left-hand side of the page.
4. Click on "Add Person" icon located at the bottom of the page.
5. Fill all the required field - "First & Last Name", "Phone Number" , "Email" , "Job Title" , "Organization / Company" , "Location".
6. Fill the phone number field with invalid formate or too short/long input.
7. Click the "Save Changes" button on the bottom of the form.
**Expected Results**: A validation error message should appear indicating that the phone number format is invalid, and the contact should not be saved.
**Actual Output**: Contact saved without any warning/error message.

## Edge Scenarios
**Test Case ID**: ES001
**Description**: Save contact with maximum allowed characters (255+) in the name field.
**Steps**:
1. Navigate to "https://linqapp.com/welcome"
2.  a.If you're a new member,Sign Up using any method: Phone Number/ Email/ Apple Account/Google Account/ LinkedIn Account
    b.If you're an existing member, Login using Phone Number/ Email/ Apple Account/ Google Account/ LinkedIn Account.
3. Once logged in,  Click on "Contacts" on the left-hand side of the page.
4. Click on "Add Person" icon located at the bottom of the page.
5. In the "First & Last Name" field, enter 255 characters (e.g. repeat a letter 255 times)
6. Fill in the remaining field with valid data - "Phone Number" , "Email" , "Job Title" , "Organization / Company" , "Location".
7. Click the "Save Changes" button on the bottom of the form.
**Expected Results**:Contact is saved successfully if 255+ characters is within the limit; otherwise, an appropriate error message should be displayed (e.g. "Name too long").
**Actual Output**: Contact saved successfully with the 255+ characters in the name filed and received confirmation pop-up on the screen.

**Test Case ID**: ES002
**Description**: Save contact only with special characters in the name field.
**Steps**:
1. Navigate to "https://linqapp.com/welcome"
2.  a.If you're a new member,Sign Up using any method: Phone Number/ Email/ Apple Account/Google Account/ LinkedIn Account
    b.If you're an existing member, Login using Phone Number/ Email/ Apple Account/ Google Account/ LinkedIn Account.
3. Once logged in,  Click on "Contacts" on the left-hand side of the page.
4. Click on "Add Person" icon located at the bottom of the page.
5. In the "First & Last Name" field, enter special characters (e.g. "@#^*#!!")
6. Fill in the remaining field with valid data - "Phone Number" , "Email" , "Job Title" , "Organization / Company" , "Location".
7. Click the "Save Changes" button on the bottom of the form.
**Expected Results**:
- If special Charecters are allowed: The contact should be saved successfully with the entered name.
- If special characters are not allowed: A validation error message should appear(e.g., “Invalid characters in name”)
**Actual Output**: Contact saved successfully with the only special charecters in the name filed and received confirmation pop-up on the screen.

**Test Case ID**: ES003
**Description**: Save contact with emojis in the name field.
**Steps**:
1. Navigate to "https://linqapp.com/welcome"
2.  a.If you're a new member,Sign Up using any method: Phone Number/ Email/ Apple Account/Google Account/ LinkedIn Account
    b.If you're an existing member, Login using Phone Number/ Email/ Apple Account/ Google Account/ LinkedIn Account.
3. Once logged in,  Click on "Contacts" on the left-hand side of the page.
4. Click on "Add Person" icon located at the bottom of the page.
5. In the "First & Last Name" field, enter emojis (e.g. "😊👨‍💻🔥")
6. Fill in the remaining field with valid data - "Phone Number" , "Email" , "Job Title" , "Organization / Company" , "Location".
7. Click the "Save Changes" button on the bottom of the form.
**Expected Results**:Contact should either be saved successfully (if emojis are allowed) or an appropriate validation error should appear.
**Actual Output**: Contact saved successfully with the emojis in the name filed and received confirmation pop-up on the screen.


## Login page test case
**Test case ID** : TS001
**Description**: Verify the correct heading is displayed when signing up with a phone number.
**Steps**:
1. Navigate to "https://linqapp.com/welcome"
2. Click Sign Up/Log in
3. Select Phone Number as the signup/Log in method.
4. Enter a valid phone number.
5. Click Continue.
6. Observe the heading on the OTP verification page.
**Expected Results**:The page should display a heading such as "Confirm OTP" or "Verify Phone Number" to match the signup method.
**Actual Output**: It is displaying "Confirm Email" heading for Phone Number signup method