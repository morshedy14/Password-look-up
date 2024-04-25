# Wi-Fi Network Extractor and Emailer

This project provides a script that extracts Wi-Fi network profiles and corresponding passwords from a Windows system and sends this information via email. It utilizes the `subprocess` module to execute system commands, `re` for regular expression processing, and `smtplib` to send emails.

## Table of Contents
1. [Installation](#installation)
2. [Usage](#usage)
3. [Dependencies](#dependencies)
4. [Security Considerations](#security-considerations)
5. [Troubleshooting](#troubleshooting)

## Installation

Ensure that you have Python installed (3.x or later) and that your environment includes the following standard libraries:
- `subprocess`
- `re`
- `smtplib`
- `email.message`

## Usage

1. Open the script and update the following:
   - `email["from"]`: The sender's email address (your email).
   - `email["to"]`: The recipient's email address.
   - `smtp.login()`: The email and password to log into the SMTP server (Gmail account).

2. If using Gmail, ensure that your account settings permit less secure apps or enable App Passwords for SMTP authentication.

3. Run the script. It will:
   - Extract a list of saved Wi-Fi profiles.
   - Retrieve and capture the corresponding passwords.
   - Construct an email message with the SSID and password for each Wi-Fi network.
   - Send the email to the specified recipient.

## Dependencies

- Windows operating system.
- SMTP email service (like Gmail).

## Security Considerations

This script involves handling sensitive information such as Wi-Fi network names and passwords. Be aware of the following security implications:

- **Email Security**: Emails can be intercepted or compromised. Ensure that you use a secure email server and consider encrypting sensitive data.
- **Gmail Authentication**: If using Gmail, ensure that you've properly secured your account. Consider using App Passwords instead of allowing "less secure apps."
- **Script Storage**: Store this script securely to prevent unauthorized access.

Always use this script in compliance with laws and regulations related to data privacy and security.

## Troubleshooting

If you encounter issues, consider the following:

- **Email not sent**: Check the SMTP configuration, ensure correct email credentials, and verify internet connectivity.
- **Wi-Fi profiles not extracted**: Ensure that you're running the script on a Windows system and that you have sufficient permissions to execute system commands.
- **Regular expression errors**: Check if the regular expressions are correctly capturing the expected output from the `netsh` commands.

If problems persist, consult online resources or seek assistance from a knowledgeable developer or security professional.
