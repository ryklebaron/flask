# Python and hasing with Flask lab

# Running the web-app
Run the web-app with the command:
```
python3 password-evolution.py
```
This will start the webapp in the foreground.

# Add user to the sqlite database
Open a second terminal to add users in the database with the following command:
> The database will be automatically created when executing the command below):
> Not hashed command: 
```
curl -k -X POST -F 'username=henk' -F 'password=differentpassword' 'https://192.168.1.149:5000/signup/v1'
```
> Note the V1 at the end of the line. This means no hashed values

> Hashed command:
```
curl -k -X POST -F 'username=henk' -F 'password=differentpassword' 'https://192.168.1.149:5000/signup/v2'
```
> Note the V2 at the end of the line. This means hashed values

# Test.db
If everything works, there is a sqlite database file in your working tree with the name "test.db".
You can browse the file with a **DB Browser for SQLITE**.

# DB Browser for SQLITE
1. Open DB Browser for SQLITE and select the **Open Database**.
2. Navigate to your **test.db**.
3. Click on **Browse Data**
> You can now see the hashed or unhashed passwords.
