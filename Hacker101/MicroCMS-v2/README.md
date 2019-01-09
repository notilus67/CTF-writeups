# Micro CMS v2
Similar to v1, try to create new pages firstly.

Now that we need username and password, the admin account may be necessary.
If we input ' into username box, we'll get a page with error message; so we can assume that 'username' is an injection point.

## 1st flag

### This is a way of automatic injection.

To utilise the injection point, we send the request to sqlmap.

Then all the tables and its contents will be listed out, and we will see the 1st flag.

## 2nd flag

Use the account and password in the user table to login, and we will see the 2nd flag.

## 3rd flag

In v2, we are not expected to edit or create the pages even we have tried to login.

We can imitate the editting request from the communication in v1, replay it in v2, and see what will happen.

The 3rd flag will come out.
