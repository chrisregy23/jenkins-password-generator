# Jenkins Password Generator

This project demonstrates a Jenkins pipeline that runs a Python script to generate secure passwords with user-defined complexity requirements.

## Features

- Accepts user-defined parameters:
  - Minimum total length
  - Minimum number count
  - Minimum special character count
- Generates a random password that meets the defined rules
- Executed through a Jenkins Declarative Pipeline
- Jenkins pulls the code from GitHub and displays the result in the console

## Files

- `generate_password.py` — Python script for generating the password
- `Jenkinsfile` — Pipeline definition to run the script with parameters

## How to Use

1. Clone the repository.
2. Set up a Jenkins pipeline job pointing to this repository.
3. Provide input parameters through the Jenkins UI.
4. Run the job and get your password in the console output.

