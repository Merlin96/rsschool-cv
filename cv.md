![wepik-clean-curriculum-vitae-202288-165253](https://user-images.githubusercontent.com/49298783/189104587-45e24e72-a68d-4a1e-9d31-a291385d8ee4.png)
English level: Intermediate
```
class User:
    def init(self,id,login,password,role):
        self.__id=id
        self.__login = login
        self.__password= password
        self.__role = role

    @property
    def get_id(self):
        return self.__id
    @get_id.setter
    def set_id(self,id):
        self.__id = id
    @property
    def login(self):
        return self.__login
    @login.setter
    def login(self,login):
        self.__login = login
    
    ##
    @property
    def password(self):
        return self.__password
    @password.setter
    def password(self,password):
        self.__password = password
    
    ##
    @property
    def get_role(self):
        return self.__role
    @get_role.setter
    def set_role(self,role):
        self.__role = role
    
    def DisplayInfo(self):
        print(self.__login)
        return self
    def toString(self):
        print(self.__id," ",self.__login," ",self.__password," ",self.__role )
        return self
    def enter(self):
        k=0
        login=input("Login: ")
        password = input("Password: ")
        while True:
            for user in range(0,10):
                if(login==users[user].login and password==users[user].password):
                    k=user
                    print("Entered")
                    while True:
                        print (k)
                        print("1 edit login ")
                        print("2 change password ")
                        print("3 delete acc")
                        print("4 Show all")
                        print("0 exit")
                        count = int(input())
                        if count==1:
                            newlog=input("New login: ")
                            users[k].login = newlog
                            print("Your new login: ", users[user].login)
                        elif count==2:
                            newpass=input("New password:")
                            users[k].password=newpass
                            print("password changed!")
                        elif count==3:
                            users.pop(user)
                            print("Deleted!")
                            for user in users:
                                user.toString()
                            User.enter(users)
                            
                        elif count==4:
                            for user in users:
                                user.toString()
                        elif count==0:
                            exit()
                        else:
                            print("Enter a valid num!")
                else:
                    pass
                    
        
        return self


kekw = User(0, "kekw", "memes", "admin")
sheeesh = User(1, "sheeesh", "ron", "user")
meeesh = User(2, "kekw", "ran", "admin")
kawaii = User(3,"kawaii", "mawaii", "admin")
weewee= User(4,"weewee", "sun", "user")
lorem = User(5,"lorem","ipsum","admin")
space = User(6,"space","earth","admin")
cat = User(7,"cat","kit","user")
dog = User(8,"dog","god","user")
whale = User(9,"whale","big","admin")
users = [kekw,sheeesh,meeesh,kawaii,weewee,lorem,space,cat,dog,whale]

for i in users:
    i.DisplayInfo()
for user in users:
    user.toString()
User.enter(users)
```
