ئل
<img src=''>
<هئل >
صثب
# BRUTE-FORCE-WP
This code is a Python script to perform brute force attacks on WordPress that uses the sites.txt text file as a list of target sites.

# WordPress Brute Force Tool

## Introduction

This Python script is designed for testing the security of WordPress installations by attempting to gain unauthorized access through brute force attacks. It specifically targets vulnerabilities in the WordPress JSON API and XML-RPC functionalities.

## Requirements

- **Python 3.x**: Ensure you have Python installed on your system.
  
- **Requests Library**: This script relies on the `requests` library for making HTTP requests. Install it via pip:
  
  bash
  
  Copy code
  
  `pip install requests`
  

## Usage Instructions

To use the script, follow these steps:

1. Create a text file named `sites.txt` containing the target WordPress URLs, one per line. Example:
  
  arduino
  
  Copy code
  
  `http://example1.com http://example2.com`
  
2. Run the script from your terminal or command prompt:
  
  bash
  
  Copy code
  
  `python script_name.py sites.txt`
  
  Replace `script_name.py` with the actual name of your script file.
  

## Script Functions

The script contains several key functions, each serving a specific purpose:

### 1. URLdomain(site)

- **Purpose**: Validates and formats the provided URL.
- **Functionality**: Ensures that the URL starts with `http://` or `https://` and ends with a `/` for proper API calls.

### 2. informations(url)

- **Purpose**: Retrieves usernames from the WordPress JSON API.
- **Functionality**: Checks for the existence of usernames and attempts to brute force them using a list of common passwords.

### 3. bf(url)

- **Purpose**: Executes brute force login attempts.
- **Functionality**: Utilizes a predefined list of common usernames and passwords to gain access.

### 4. xlmprc(url, username, password)

- **Purpose**: Validates credentials via XML-RPC.
- **Functionality**: Sends a login request to the XML-RPC endpoint and checks for successful authentication.

### 5. wp_login(url)

- **Purpose**: Attempts to log in as an administrator.
- **Functionality**: Uses a standard username (`admin`) and a common password (`admin`) to attempt a login.

### 6. userpro(url)

- **Purpose**: Registers a new user if the UserPro plugin is active.
- **Functionality**: Submits a registration form to create a new user account.

### 7. vln(url)

- **Purpose**: Attempts to create a new admin user via the wpgateway plugin.
- **Functionality**: Sends a request to create a user with predefined credentials.

### 8. main(url)

- **Purpose**: Main execution function for processing each URL.
- **Functionality**: Coordinates all the tasks of checking URLs, retrieving usernames, and performing login attempts.

## Output

- **Panels.txt**: The script logs successful login attempts in this file, formatted as follows:
  
  bash
  
  Copy code
  
  `url/wp-login.php#username@password`
  

## Important Considerations

- **Legal and Ethical Use**: This script is intended for educational purposes and should only be used on websites that you own or have explicit permission to test. Unauthorized access to computer systems is illegal and unethical.
- **Testing Environment**: It is recommended to use this script in a controlled testing environment to avoid potential legal issues.

## Conclusion

The WordPress Brute Force Tool is a powerful script for security testing. Proper understanding and usage can help in identifying vulnerabilities in WordPress sites and enhancing their security measures.
