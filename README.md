# Insecure Blog

A very insecure blog app that is designed to be attacked.

### Setup

To start, don't look at the code.  Try to figure out as much as you can before looking at the code.

```
rake db:create
rake db:migrate
rake db:seed
```

## Possible Attacks

1. __Brute force account access__.  The app was written with very bad password validation.  Try to write a script that will brute force the password.  __HINT__: Even though there is no link to all of the restful routes for a user, they are still accessible from the URL.  It may help you get the information you need.

##Access other users information by passing in the nesseccary query. i.e. localhost:3000/users/3, will give you access to user 3.

Can delete users witout every logging in.

Created users get is_admin privileges... weird
##

2. __Password__: Something about the password create is not to secure.
##
pasword_digest is passed into the private method in te users controller. You should not be doing this.

##

2. __Simple escalation of privileges__: Certain features of the app are not restricted properly.  Find out which features those are and prove that is exploitable.
3. __Escalation of privileges++__: It is possible in the app to have admin power through signup.  Figure out how.
4. __Session Hijacking__: There are many insecurities about the session.  Try decrypting the session.  What do you see?  What else about the session is not secure?
5. __CSRF__: Prove that the site can be hacked with CSRF.
6. __SQL Injection__: Find a sql injection attack in the site
