# python_oops_Entry-Registration
It is entry registration for events 
OOPS concepts:
  inheritance 
  
Here the DB consist of all the users anme and password hash password was used to store the password in hidden form

->salt=hashlib.sha256(os.urandom(60)).hexdigest().encode('ascii')

it was randomly generated number from the os(secured hash algorithm -256) in the format hexadigit which is stored as a ascii value(i.e.string)
->pwdhash=hashlib.pbkdf2_hmac('sha256',password.encode('utf-8'),salt,100)

Here "password based key drivation function" (hash_name,password,salt,no_of_iterations,dklen(length of the password))
  #pbkdf2 can only handle bytes
          salt is already converte d as bytes(i.e ascii:0-9,a-z)-string to hex
          password was converted to UTf-8(i.e:a-z)
-> pwdhash=binascii.hexlify(pwdhash)=Now the generated key is converted into hexadecimal value

->return (salt+pwdhash).decode('ascii')=Here both the salt value and hash was concatenated and decode to ascii format hex->string or storing purpose

utf-  is character encoding format (unicode transformation format)

class method-the things which are not going to be changed depods on the instance and only works on class variblaes


instance method -when we work on instance variables


static method- when we doesn't work onn class and instance vaiables
 


class 
  DB-consists of name and password
  Methods:
    static-hash password-hash the password and store the password while registraion
    static-verify password-chec
    
  login-authenticates the user
  Methods:
    classmethod-check_user
    normal method-search_index
  Register
   Methods:
    class method-storing 
    
  show events
  
  myevents
  
  update
