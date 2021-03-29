# Flask Blog
## Topics Covered
1. Templates
2. Forms with Validations
3. Database Connectivity
4. User Authentication
5. User Account, Login and Logout
6. Pagination
7. Password Reset
8. Blueprints
9. Custom Error Pages

## Setup Project
### Clone
For setting up the project, we need to clone the project using the below command.
```sh
git clone https://github.com/harshakoneru98/Flask_Blog.git
```
### Install Packages
Go to the project directory and open the command prompt. Now, install all packages required for a project using the below command.
```sh
pip install -r packages.txt
```
### Create Database
For storing data and user management, we need to create a database using the below commands.
Go to the project directory and open the python command prompt.
```sh
from flaskblog import db
db.create_all()
```
Above commands create database file in flaskblog package.

### Setting Environmental Variables 
Please follow the below steps to set necessary environmental variables for the project
1. In Search, search for and then select: System (Control Panel)
2. Click the Advanced system settings link.
3. Click Environment Variables. ...
4. In the User Variables window, click on New and enter variable name and variable value.

**Variable Name and Value**
| Name | Value |
| ------ | ------ |
| SECRET_KEY | Create Secret Key  |
| SQLALCHEMY_DATABASE_URI | sqlite:///site.db |
| EMAIL_USER | Your Email ID |
| EMAIL_PASS | Your Email Password |

**SECRET_KEY** - We use this secret key for encrypting the password.
**SQLALCHEMY_DATABASE_URI** - We are using SQLite database.
**EMAIL_USER, EMAIL_PASS** - Email Credentials for sending the password reset email for forgot password functionality.

##### Creating Secret Key
Need to create secret key for hashing password using **secrets** module. Run the below commands using Python command prompt.
```sh
import secrets
secrets.token_hex(16)
```
**Output:**
```sh
'6d7298291fb9a9867b57d6a4086058b1'
```
Copy **6d7298291fb9a9867b57d6a4086058b1** and keep it as **SECRET_KEY** value in environmental variables.

## Run Project
Go to the project directory and open the command prompt. Run the project using the below command.
```sh
python run.py
```
Open below address in your preferred browser.
```sh
127.0.0.1:5000
```

## Reference
https://www.youtube.com/playlist?list=PL-osiE80TeTs4UjLw5MM6OjgkjFeUxCYH
