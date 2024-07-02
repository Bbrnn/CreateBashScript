# Linux User Creation Bash Script

## Overview
This project involves creating a Bash script called create_users.sh that reads a text file containing employee usernames and group names, creates the specified users and groups, sets up home directories with appropriate permissions and ownership, generates random passwords for the users, and logs all actions. Additionally, it stores the generated passwords securely.

## Prerequisites

    * Ensure you have root or sudo privileges to execute the script.
    * Create a text file (e.g., users.txt) with the user and group information formatted as username;group1,group2,....

Example users.txt:
light; sudo,dev,www-data
idimma; sudo
mayowa; dev,www-data

**Script Details**
Features

    User and Group Creation:
        Creates users as specified in the text file.
        Each user is assigned to their personal group, matching their username.
        Assigns users to additional groups as specified.

    Home Directory Setup:
        Creates home directories for each user.
        Sets appropriate permissions and ownership.

    Password Generation:
        Generates random passwords for each user.
        Stores passwords securely in /var/secure/user_passwords.txt.

    Logging:
        Logs all actions to /var/log/user_management.log.

    Error Handling:
        Handles scenarios where users or groups already exist.
        Provides meaningful error messages.

Usage

    Clone the repository:

    bash

git clone <repository_url>
cd <repository_directory>

Make the script executable:

bash

chmod +x create_users.sh

Run the script:

bash

sudo ./create_users.sh users.txt

