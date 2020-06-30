# password_checker
A tool to check if a password has ever been leaked during a data breach using haveibeenpwned without sending the full password to the API.

Click here for a live, interactive version of the code:
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/kdhenderson/password_checker/master)

This is the process the program follows:
  - The user enters a password(s) through the command line using the sys library.
  - A hashed password is generated with a SHA-1 hashing function using the hashlib library.
  - The first 5 characters of the hashed password are sent to the haveibeenpwned API using the requests library, and the API responds with leaked passwords from its database that match the starting hash.
  - On the local machine, the program checks the response data for a match to the rest of the hashed password and returns if a match exists and how many times the password has been pwned.


Install the requirements using pip install -r requirements.txt.
  - Make sure you use Python 3.
  - You may want to use a virtual environment for this.
 

Usage:
 - Run the program from the command line.
 - Enter password(s) as arguments like this: $ python3 checkmypass.py password1 password2 etc
