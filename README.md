# PHP and MySQL Voting System Documentation

## Introduction

This documentation outlines the design and implementation of a simple voting system using PHP and MySQL. The system allows users to cast votes for predefined options and stores the results in a MySQL database.


### Description : 
In "ONLINE VOTING SYSTEM" a voter can use his/her voting right online without any difficulty. He/She has to be registered first for him/her to vote. Registration is mainly done by the system administrator for security reasons. The system Adminstrator registers the voters on a special site of the system visited by him only by simply filling a registration form to register voter.
After registration, the voter is assigned a secret Voter ID with which he/she can use to log into the system and enjoy services provide by the system such as voting. If invalid/wrong details are submitted, then the citizen is not registered to vote.


## Features

1. **User Authentication:**
   - Users must log in to cast their votes.
   - User accounts are stored in the MySQL database.

2. **Voting Options:**
   - Admins can define voting options through the admin panel.
   - Options are stored in the MySQL database.

3. **Voting Process:**
   - Users can view available options and cast their votes.
   - Each user can only vote once for a particular poll.

4. **Admin Panel:**
   - Admins have a secure panel to manage polls, view results, and add/remove options.

5. **Database Schema:**
   - `users` table: stores user information (id, username, password hash).
   - `options` table: stores available voting options (id, option_text).
   - `votes` table: records user votes (id, user_id, option_id).

## Installation

1. **Database Setup:**
   
  Create a database `poll`.
  
  import `poll.sql` file from phpmyadmin.


2. **User Authentication:**
   
   ```ADMIN LOGIN DETAILS 
  URL: localhost/online_voting/admin 
  Email : admin@gmail.com 
  Password : admin 
  ```

3. **Voting Pages:**
   - Implement pages for users to view polls, options, and cast votes.
   - Ensure proper error handling and validation.

4. **Admin Panel:**
   - Protect the admin panel with authentication.
   - Create pages to manage polls, view results, and add/remove options.

## Security Considerations

1. **Input Validation:**
   - Validate all user inputs to prevent SQL injection and cross-site scripting (XSS).

2. **Password Security:**
   - Use strong password hashing algorithms and salt passwords.

3. **Session Management:**
   - Implement secure session handling to prevent session hijacking.

4. **Admin Privileges:**
   - Only grant admin privileges to trusted users.

## Usage

1. **User Registration:**
   - Users must register for an account before voting.

2. **Admin Login:**
   - Admins can log in to the admin panel using their credentials.

3. **Define Polls:**
   - Admins can add new polls, define voting options, and manage existing polls.

4. **Voting:**
   - Users log in, view available polls, and cast their votes for chosen options.

5. **View Results:**
   - Admins can access the admin panel to view real-time voting results.

## Conclusion

This PHP and MySQL voting system provides a secure and scalable solution for conducting online polls. It ensures proper user authentication, input validation, and an admin panel for easy management. Customization options are available to suit specific voting needs.

For detailed instructions, refer to the provided documentation and comments within the code.
