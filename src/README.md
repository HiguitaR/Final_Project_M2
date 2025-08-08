# **Module 2 Project: Customer Management System**
- This project aims to implement and integrate all the `Object-Oriented Programming` concepts 
discussed in Module 2. You will design and build a basic system that allows you to 
manage users, differentiate their permissions through roles, and record a history of 
their actions.
---

## **1. User Management**
- The system must maintain a record of multiple users.
- Each user in the system must have the following associated information:
  - A full name.
  - A unique user ID to identify the user in the system.
  - A unique username used for login.
  - A password (for simplicity, it will be handled as a simple text string, without applying advanced cryptographic techniques).
- The system must be able to perform the following user-related operations:
  - Create new users: Add a new user to the system with their complete information.
  - Search for a user: Find a specific user, primarily by their user ID or username.
  - Update user information: Modify the full name or password of an existing user. The password can only be updated if the correct current password is provided (simple validation).
  - Delete a user: Remove an existing user from the system.
---
## **2. User Roles and Permissions**
- There are different roles that can be assigned to users. Initially, the system must support at least two roles: "Administrator" and "Standard."
- Each user must be assigned a unique role in the system.
- Operations on users are restricted based on the role of the user attempting to perform them:
  - Only users with the "Administrator" role have permission to create, delete, and update information for any user in the system (including that of other administrators).
  - Users with the "Standard" role only have permission to view and update their own profile information. They cannot create, delete, or update information for other users.
---

## **3. Action History**
- The system must record an Action History for each user.
- Each recorded action must include:
  - A description of what the user did (e.g., "Logged in," "Updated profile," "Created user John").
  - A timestamp indicating when the action occurred (this can be a simple number, such as the result of System.currentTimeMillis()).
- Each user must have their own action history. Actions recorded for a user logically belong to that user and not to another.
- The system must allow recording an action for a specific user.
- The system must allow displaying the complete history of actions for a specific user.
---

## **4. Login (Simulated)**
- The system must include a basic function to simulate a login.
- This function must receive a username and password.
- If the username and password match those of a registered user in the system, the function must indicate that the login was successful and provide access to the user's information (returning the user object, for example).
- If the credentials do not match, the function must indicate that the login failed.