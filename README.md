## ePortfolio

### Professional Self-Assessment

  In completing the Computer Science program I have learned all the skills needed to perform as a competent developer with a 
thorough understanding of design, data structures, workflow and teamwork principles.  What began as 
an interest in coding grew into a passion for software design and technology, and the CS program helped me 
define an interest specifically in backend and cloud services. Completing my courses and working as an intern 
has prepared me to meet the expectations and fulfill the responsibilities of a developer role and to understand 
my place in the field of software engineering and development. I have learned to code, but I have also learned 
engineering and design principles, team collaboration skills and an understanding of the relationship between 
developers, stakeholders and users. 

  In my time in the CS program and during my internship on a backend operations team, I learned a lot about cloud service 
maintenance, data structures and security, as well as general knowledge about the field of software development, testing,
debugging and much more. I learned a lot about the workflow and general responsibilities of a developer and became familiar 
with services like Confluence and Jira as well as Agile practices. During my internship I was mentored and worked every day 
with a small team of 3 developers, usually working on debugging tickets together for several hours at a time over a Teams meeting. 
I was assigned several bug and feature update tickets, many of which were directly user-facing. I worked in workflow automation 
services such as Jenkins, database and querying services such as elasticsearch and mysql, and testing services like POSTman, as 
well as writing code directly and using git to commit and push code to BitBucket. I automated several unit and integration tests, 
as well as writing code to meet functional requirements.  I became very familiar with AWS cloud services where most of our own 
services were hosted and managed, as well as the security principles and mindfulness needed for accessing the multitude of cloud 
resources and production codebases.  Debugging every day required me to look beyond just the code and understand the many working 
parts of a service, and to see the bigger picture of software engineering and architecture. An example of a ticket I completed 
during my time there was writing an exponential backoff retry function to solve a deadlock error caused when one of our clients 
accessed a mysql database with several devices. 

  Aside from my work directly with development, I was also given the opportunity during my internship to sit in on several meetings
and see how the entire process of software design flows. I sat in on meetings with stakeholders and product managers as developers 
discussed functional requirements and time expectations. I sat in on sprint planning and sprint retrospective meetings. I also spent
a lot of time writing and updating documentation on Confluence like testing plans, feature or function justifications and updated 
functionality. All of my experiences and work during my courses and internship have helped to refine my professional focus in the 
field to cloud services, backend development and operations. My professional goal is to enter the field as a backend developer with 
a focus on AWS.  

  The artifact I developed during the CS Capstone course demonstrates my software design ability, as well as my understanding of how multiple services can communicate and interact with algorithms and data structures. I met the course outcomes of the capstone project and demonstrated my ability to meet functional requirements. This artifact works as a ???password locker??? program, storing and encrypting information behind a master password. The program can also store data in a mysql database. The program is a fully-interactable command line program and was written with an end-user in mind. I met course outcome 1 in enhancement 1 by enhancing the existing CRUD functions into more robust and reusable functions. The code is up to best practices and industry standards. I met course outcome 2 in all 3 enhancements by updating the code to be clearer, better-commented and up to best practices. By condensing my code into modules, classes and objects, the code can be read and worked on by any developer and can be easily scaled. I demonstrated in each enhancement the value of the functionality I was implementing into the project. I met course outcome 3 in enhancement 2 by researching and implementing an algorithmic solution into my project that added value and purpose to the overall functionality. The functionality added by the enhancements has purpose and intention. I met course outcome 4 in enhancements 1 and 3 by implementing a database solution as a data backup option. I wrote code that interacts with a mysql database to store and update your data. The code throughout the project is up to industry standards with exception handling and anticipation of user/service errors. I met the final course outcome in enhancements 1 and 2. In enhancement 1, I demonstrated my knowledge of a securely-designed program in my execution of the code with appropriate levels of abstraction, the use of config and initializing files and the implementation of a master password functionality. In enhancement 2, I implemented an encryption algorithm to encrypt and protect the data stored by the program. 

This project demonstrates my ability to research and implement solutions to meet requirements and intended outcomes. It shows my ability to build and design functional and reusable code that meets best practices and can be collaborated on by any other developer. My code is compartmentalized and abstracted to an appropriate level. I researched solutions to the algorithm and database sections of the requirements for the project and implemented them into the program. The three enhancements all come together to complete the functionality of the project and all work together with purpose and intention. The three enhancements together show my ability as a developer to grasp the different aspects of software development and bring them together into one functional project to display my skills.

  In developing this project I have met the 5 course outcomes of the Capstone course with the following enhancements to the original code, which I explain in further detail in the accompanying narrative sections:
  
[CS-499-01] Employ strategies for building collaborative environments that enable diverse audiences to support organizational decision
making in the field of computer science:

  _Enhancement 1_
  
[CS-499-02] Design, develop, and deliver professional-quality oral, written, and visual communications that are coherent, technically sound,
and appropriately adapted to specific audiences and contexts:

  _Enhancements 1 and 2_
  
[CS-499-03] Design and evaluate computing solutions that solve a given problem using algorithmic principles and computer science practices and
standards appropriate to its solution, while managing the trade-offs involved in design choices (data structures and algorithms):

  _Enhancement 2_
  
[CS-499-04] Demonstrate an ability to use well-founded and innovative techniques, skills, and tools in computing practices for the purpose of
implementing computer solutions that deliver value and accomplish industry-specific goals (software engineering/design/database):
  
  _Enhancements 1 and 3_
  
[CS-499-05] Develop a security mindset that anticipates adversarial exploits in software architecture and designs to expose potential vulnerabilities,
mitigate design flaws, and ensure privacy and enhanced security of data and resources:
  
  _Enhancements 1 and 2_
  
  
### Original Code
[CS340 Project 2 Code](https://github.com/jordan-davis8snhu/CS-340)
### Code Review
[![Code Review](http://img.youtube.com/vi/ZrCT1JraBn8/0.jpg)](http://www.youtube.com/watch?v=ZrCT1JraBn8 "CS499 Capstone Project Code Review")
### New Artifact
[The New Artifact Code](https://github.com/jordan-davis8snhu/CS499_Pylock) (The same artifact is used for all enhancements)

### Enhancement 1

_1. Briefly describe the artifact. What is it? When was it created?_

  The original artifact was a project from CS-340 Client/Server Development. The original artifact was a python script that interacted with mongodb through CRUD operations:
  
```python
class AnimalShelter(object):
    """ CRUD operations for Animal collection in MongoDB """

    def __init__(self,user,password):
        # Initializing the MongoClient. This helps to 
        # access the MongoDB databases and collections. 
        self.client = MongoClient('mongodb://%s:%s@localhost:35825'%(user,password))
        self.database = self.client['AAC']

    # Complete this create method to implement the C in CRUD.
    def create(self, data):
        if data is not None:
            self.database.animals.insert_one(data)  # data should be dictionary
            print("++++++++++++++++++ animal created successfully+++++++++++++++")
        else:
            raise Exception("Nothing to save, because data parameter is empty")
            
    # THIS IS A READ METHOD
    def read(self, data):
        if data is not None:
            data = self.database.animals.find(data,{"_id":False})  # data should be dictionary   
            return data
        else:
            raise Exception("nothing to read, hint is empty")
            
            
    # this method will receive a dictionry, find all items that matvh the dictionary 
    #values and delete them


    def delete(self, _data):
        if _data is not None:
            data = self.read(_data) # checj if animal exists
            if data is None:
                print("Animal not found")
                return
            #if found delete the animal or animals
            self.database.animals.delete_many(_data)  # data should be dictionary 
            data = self.read(_data) #confirm if animal was deleted
            return data
        else:
            raise Exception("nothing to read, hint is empty")
            
    # this method update usin the id of the collection, one can also update using any key
    def update(self, _keys,_data):
        if _data is not None and _keys is not None:
            self.database.animals.update_many(_keys,{'$set':_data})  # _keys will check for the doc to update 
            data = self.read(_data)
            return data
        else:
            raise Exception("please nter both key and data to modify the collection")
```
```python
###########################
# Data Manipulation / Model
###########################
# FIX ME update with your username and password and CRUD Python module name

username = "aacuser"
password = "aacuser"
shelter = AnimalShelter(username, password)


# class read method must support return of cursor object and accept projection json input
df = pd.DataFrame.from_records(shelter.read({}))


#########################
# Dashboard Layout / View
#########################
external_stylesheets = ['https://codepen.io/chriddyp/pen/bWLwgP.css']                            
app = JupyterDash('SNHU CS340')

#FIX ME Add in Grazioso Salvare???s logo
image_filename = 'GSLogo.png' # replace with your own image
encoded_image = base64.b64encode(open(image_filename, 'rb').read())
```

  I took the concept of the CRUD operations and database interaction and expanded on the idea to create something like a password locker. The enhanced artifact is based on the CRUD operations. I have based a new application around them in which the user can store username/password combinations and secure them behind a master password. It functions as a command-line program, which is another enhancement on the original artifact. I created this artifact in the last week as an enhancement of the original project. 

_2. Justify the inclusion of the artifact in your ePortfolio. Why did you select this item? What specific components of the artifact showcase your skills and abilities in software development? How was the artifact improved?_

  I decided to create and include this project in my ePortfolio because the level of enhancement demonstrates what I have learned about software design in the CS program. The original project was a simple, short script. From that basic functionality I have created a project all of my own with many moving parts and greatly increased functionality. It is a practical, usable program and I have organized it in a professional manner. The artifact also demonstrates my understanding of OOP and modularization of code. Whereas the original project was a single-file script, I now have a full-fledged project that includes multiple directories, function-specific files, a config.py, a master.py and a requirements file. I wrote several classes for this project, containing the appropriate functions, and apply the classes by creating objects and calling the functions. Functions and variables have appropriate and obvious names. Many of the variables are abstracted to the appropriate level and are not hardcoded into the variables themselves. I hardcoded as few things as possible, I think I may have 0 hardcoded values in this project. I have used a config.py and an initialize.py appropriately, which I believe illustrates my understanding of how developers engineer projects to be as modular and configurable as possible:
  
```python
# Locker class contains the CRUD functions
class Locker:

    login_list = []

    def __init__(self, service: str, user: str,  path: str):
        """

        :param service:
        :param user: associated user name
        :param path: password path
        """
        self.path = path
        self.service = service
        self.user = user

    def get_logins(self):
        self.login_list = []
        with open(self.path, 'r') as f:
            for login in f:
                self.login_list.append(json.loads(login))

        return self.login_list

    def set_logins(self):
        with open(self.path, 'w') as f:
            for d in self.login_list:
                f.write(json.dumps(dict(d)))
                f.write('\n')

    def get_login_dict(self):
        for d in self.login_list:
            if self.service in d:
                if self.user in d[self.service]:
                    return d

    def create(self, db: str, cursor: str, password: str):
        """

        :param password: associated password
        :return:
        """
        self.get_logins()

        d = self.get_login_dict()
        if d is not None:
            response = 'credentials already exist'
            return response
        else:
            login = {
                self.service: {
                    self.user: password
                }
            }
            with open(self.path, 'a+') as f:
                f.write(json.dumps(dict(login)))
                f.write('\n')

            try:
                data.insert_data(cursor, db, self.service, self.user, password)
            except Exception as e:
                print(e)
                pass

            response = 'login created'
            return response

    def read(self):
        self.get_logins()

        d = self.get_login_dict()
        if d is None:
            response = 'credentials invalid'
            return response
        else:
            password = (d[self.service][self.user])
            return password

    def delete(self, cursor, db):
        self.get_logins()

        d = self.get_login_dict()
        if d is None:
            response = 'credentials invalid'
            return response
        else:
            del(d[self.service])
            self.set_logins()

            try:
                data.delete_data(cursor, db, self.service, self.user)
            except Exception as e:
                print(e)
                pass

            response = 'deletion successful'
            return response

    def update(self, cursor: str, db: str, new_pass: str):
        """

        :param new_pass: updated password
        :return:
        """
        self.get_logins()

        d = self.get_login_dict()
        if d is None:
            response = 'credentials invalid'
            return response
        else:
            d[self.service][self.user] = new_pass
            self.set_logins()

            data.update_data(cursor, db, self.service, self.user, new_pass)
            response = 'credentials updated'
            return response
```

  
  All project-wide variables are configured in the config. This makes the project easily readable and updatable, and the code is easy to follow and understand just by following the workflow through the code. I believe this also benefits the project???s security, since the values are not directly exposed and can be easily updated. Nothing in the code itself exposes the user. Next to all this, I have also successfully converted the project into a command-line application, which can execute a variety of user commands (this is where the CRUD operations come into play). I also did a fair amount of exception handling. I believe this enhancement shows my understanding and ability to apply software design and engineering skills.

_3. Did you meet the course objectives you planned to meet with this enhancement in Module One? Do you have any updates to your outcome-coverage plans?_

  With this artifact enhancement, I have met or am close to meeting 3 of the course outcomes. In combination with upcoming algorithm/database enhancements, I will meet all of them. The three this artifact accomplishes or begins to accomplish are:
  
_[CS-499-01] Employ strategies for building collaborative environmentsthat enable diverse audiences to support organizational decision making in the field of computer science_

For many of the reasons stated above. The code is up to standard practices; commented, modularized and abstracted to the appropriate degree, uses a config and standard service organization of directories, files, classes, functions and variables that would be familiar to other developers. Since the program is built to use commands, I have also written a brief readme on how to use the program which I will later expand on. I tried to make the code itself as readable as possible, and others familiar with code would be able to read through it and understand what it is doing and what the workflow through the service is like.

_[CS-499-02] Demonstrate an ability to use well-founded and innovative techniques, skills, and tools in computing practices for the purpose of implementing computer solutions that deliver value and accomplish industry-specific goals_

With this enhancement I accomplished a robustly designed project that imitates the design/architecture/engineering of what you might see in a real industry service. The service is very modularized and abstracted, and I did a good amount of appropriate exception handling to anticipate service errors or user errors. As far as using innovative skills, techniques and tools, I accomplished this by creating the command-line functionality. I turned the artifact into an executable service that can actually be interacted with from a terminal, and it takes several commands that allow the user to interact with the service in different ways. As far as tools, I have researched and implemented external python libraries to solve complex problems, such as the pyperclip library to directly copy passwords to the clipboard and the cryptography library for data encryption. 

_[CS-499-05] Develop a security mindset that anticipates adversarial exploits in software architecture and designs to expose potential vulnerabilities, mitigate design flaws, and ensure privacy and enhanced security of data and resources_

While I don???t think this artifact fully accomplishes this outcome, it begins to address it and demonstrates my understanding of security and securely-designed services. The security of a service really does begin at the design/architecture level. For some of the reasons I have mentioned above, I have begun to touch on this outcome. For instance, the multiple levels of abstraction of variables and the use of a config file. The modularization of functionality. Using the os library to generate paths to files rather than directly exposing the path. Using pyperclip to copy a password to the clipboard when you read it, rather than directly displaying the password on screen. Implementation of a master password to protect the main files where all the other passwords are stored, so that the project has multiple levels of encryption. Hiding the encryption keys in encrypted files themselves rather than storing them inside variables. Then, the encryption itself. While this kind of project would never see real use in the professional world, and while using a fernet algorithm to encrypt text isn???t exactly industry-standard, it illustrates my understanding of a security mindset and mitigating insecure code. For example, you cannot decrypt a file and then quit the program and see the unencrypted data. There is no direct command for decryption, and the file is unencrypted and then re-encrypted with a newly-generated fernet key after each command. This is one example of my consideration of security flaws within the code design.

_4. Reflect on the process of enhancing and/or modifying the artifact. What did you learn as you were creating it and improving it? What challenges did you face?_	

I learned a lot while creating this enhancement. I was able to apply many of the things I have learned about programming and software design throughout the program. I was able to create a much more complex project than what I started with, just beginning with the CRUD operations. I learned how to use the cryptography library and began thinking with a security mindset, which led to many of my design decisions and greatly influenced how I organized the workflow and execution of the project???s functionality. I also learned the value of abstracting variables and organizing functions into classes, directories and files based on intent and functionality. I designed the project with team collaboration, modularity and configuration in mind, and tried to architect the service in a way that it is very obvious to new developers looking at it.

### Enhancement 2

_1.	Briefly describe the artifact. What is it? When was it created?_

This is the same artifact used in enhancement 1 since I developed both enhancements simultaneously. The original artifact was a project from CS-340 Client/Server Development. The original artifact was a python script that interacted with mongodb through CRUD operations. In enhancement 1, I enhanced the CRUD operations. In this enhancement, I used a fernet hashing algorithm for the purpose of encrypting text. This algorithm function works directly with the software design portion of the project, as the user commands (CRUD operations) directly use the encryption and decryption functions. The hashing algorithm is central to the design and execution of the project. Without it, the project wouldn???t make much sense. 

_2.	Justify the inclusion of the artifact in your ePortfolio. Why did you select this item? What specific components of the artifact showcase your skills and abilities in software development? How was the artifact improved?_

I decided to implement an algorithm in this way to demonstrate complex problem-solving skills and an understanding of how to research and implement programming solutions and techniques to solve specific problems/ functionality requirements. The function of the fernet algorithm is central to the project as a whole and solves a unique problem within the project- the security and obscurity of sensitive data. Since the idea was to create a password database, one of the first considerations that comes to mind is how to keep those passwords safe and ideally unreachable to prying eyes. I accomplished combining the use of the algorithm with the design of the project and handling the considerations that come with that. I designed classes and functions around the execution and specific use of the algorithm for my project, demonstrating an understanding of the value and proper use of software tools. The artifact was improved by this enhancement because it fulfills a core functionality requirement of the project. I had to design the code in a way that the user can interact with encrypted data ??? each time the data is encrypted or reencrypted, a new fernet key is generated by the algorithm. There are many times that I ran into design problems with this feature and locked myself out of the data by mismatching keys. Another algorithmic feature central to the project???s functionality is a simple random character generator.  

```python
# Generate a fernet key
def gen_key(key_file: str):
    """

    :param key_file: key path
    :return:
    """
    key = Fernet.generate_key()

    with open(key_file, "wb") as f:
        f.write(key)
        f.close()


def read_key(key_file: str):
    """

    :param key_file: key path
    :return:
    """
    with open(key_file, "rb") as f:
        key = f.read()
        f.close()
    return key


class Crypto:

    def __init__(self, path: str, key_file: str):
        """

        :param path: password path
        :param key_file: key path
        """
        self.path = path
        self.key_file = key_file

    def encrypt(self):
        gen_key(self.key_file)

        key = read_key(self.key_file)

        with open(self.path, 'rb') as f:
            data = f.read()
            f.close()

        k = Fernet(key)

        try:
            enc_data = k.encrypt(data)

            with open(self.path, 'wb') as f:
                f.write(enc_data)
                f.close()

            response = 'file encrypted'
            return response

        except cryptography.fernet.InvalidToken:
            response = 'key is invalid'
            return response

    def decrypt(self):

        key = read_key(self.key_file)

        with open(self.path, 'rb') as f:
            data = f.read()

        k = Fernet(key)

        try:
            dec_data = k.decrypt(data)

            with open(self.path, 'wb') as f:
                f.write(dec_data)
                f.close()
            response = 'file decrypted'
            return response

        except cryptography.fernet.InvalidToken:
            response = 'key is invalid'
            return response
```

_3.	Did you meet the course objectives you planned to meet with this enhancement in Module One? Do you have any updates to your outcome-coverage plans?_

With my last enhancement I touched on many of the objectives I believe this artifact accomplishes ??? the outcomes I covered in that narrative covered both the software design and the algorithm aspects of those outcomes. Since I developed both enhancements at the same time, this enhancement meets the same outcomes. There is one additional outcome that I did not cover in the last narrative that this enhancement specifically covers:

_[CS-499-03] Design and evaluate computing solutions that solve a given problem using algorithmic principles and computer science practices and standards appropriate to its solution, while managing the trade-offs involved in design choices_

The algorithm solution I implemented in this project is not superfluous ??? I did not use it just to insert an algorithm into the program, but because the function of the algorithm is central to the core functionality of the project itself. The use of the algorithm was the best possible solution for the problem that the project is trying to solve, and I had to design the rest of the code and functionality to accept and make use of the algorithm functions. While the initial idea of the project was to update the CRUD functionality, the service itself would not be very useful or practical without the use of the algorithm. On top of that, the CRUD functions had to be updated to use the encrypt and decrypt functions and operate in such a way that they can interact with the encrypted text. Therefore, the fernet hashing algorithm is as central to the project as the CRUD operations themselves. This combines the functionality and desired outcomes with the problem-solving capacity of algorithms to create a cohesive, holistic service.

_4.	Reflect on the process of enhancing and/or modifying the artifact. What did you learn as you were creating it and improving it? What challenges did you face?_	

I learned a lot while creating this enhancement. While the last enhancement allowed me to demonstrate the programming skills I have learned over the course of the program such as OOP, modularity, best practices etc., this enhancement allowed me to display my ability to problem solve and discover solutions to achieve the desired functionality of a project. I was able to research and find the best solution to fit my requirements. Of course, introducing and algorithm affects the execution and architecture of a service, so the challenges I faced involved integrating the functionality with the already existing code base. The code had to be manipulated and heavily reorganized for the algorithm to work properly and effectively.

### Enhancement 3

_1.	Briefly describe the artifact. What is it? When was it created?_

All of my enhancements are related to the same artifact. The original artifact was a project from CS-340 Client/Server Development. The original artifact was a python script that interacted with mongodb through CRUD operations. In enhancement 1, I enhanced the CRUD operations. In enhancement 2, I used a fernet hashing algorithm for the purpose of encrypting text. In this enhancement, I developed functions to create and populate a mysql database with the data in the password locker.

_2.	Justify the inclusion of the artifact in your ePortfolio. Why did you select this item? What specific components of the artifact showcase your skills and abilities in software development? How was the artifact improved?_

The artifact I have chosen to include meets all the course objectives. It uses innovative computer science techniques to solve unique problems, an algorithmic function as a solution to address specific functionality requirements, and includes database interaction to demonstrate the data structure and data manipulation on the backend of the project. The database component of my artifact demonstrates my understanding of database principles and my ability to integrate those principles into a project. It also showcases my ability to research and write code that interacts with an outside service and integrate it into an existing service. Essentially what this enhancement does is interface with the mysql program and creates/updates/deletes entries from a mysql table. The new code creates a database called ???pylock??? and a table called ???logins.??? It populates that table with the service, username and password data. It is like a soft mysql wrapper for this specific project. I also wrote a function to read data directly from the mysql table, but did not use it anywhere. You can use it from the python terminal however to read data from the database without having to directly login to mysql. The mysql permissions are set in the config.py.

```python
def create_db(cursor):

    create = "CREATE DATABASE if not exists pylock;"
    cursor.execute(create)


def drop_db(cursor):

    drop = "DROP DATABASE if exists pylock;"
    cursor.execute(drop)


def create_table(cursor):

    cursor.execute("USE pylock")

    table = "CREATE TABLE passwords ( " \
            "service  VARCHAR(16) NOT NULL," \
            "username VARCHAR(32) NOT NULL," \
            "password VARCHAR(64) NOT NULL)"

    cursor.execute(table)
    return


def insert_data(cursor, db, service, username, password):

    cursor.execute("USE pylock")

    sql = "INSERT INTO passwords (service, username, password) VALUES (%s, %s, %s)"
    val = (service, username, password)

    cursor.execute(sql, val)
    db.commit()



def select_data(cursor, service, username):

    cursor.execute("USE pylock")

    # selecting query
    query = f"SELECT password FROM passwords WHERE service = '{service}' and username = '{username}'"
    cursor.execute(query)

    result = cursor.fetchall()

    for x in result:
        print(x)


def update_data(cursor, db, service, username, password):

    cursor.execute("USE pylock")

    # selecting query
    query = f"UPDATE passwords SET password = '{password}' WHERE service = '{service}' and username = '{username}'"
    cursor.execute(query)
    db.commit()


def delete_data(cursor, db, service, username):

    cursor.execute("USE pylock")

    # selecting query
    query = f"DELETE FROM passwords WHERE service = '{service}' and username = '{username}'"
    cursor.execute(query)
    db.commit()
```

_3.	Did you meet the course objectives you planned to meet with this enhancement in Module One? Do you have any updates to your outcome-coverage plans?_

My first two enhancements covered many course outcome requirements. As planned for this enhancement, I have met a course outcome with my work on the database portion of my artifact. With this enhancement, I have touched on all 5 of the course outcomes. The course outcome I have met with this enhancement follows:

_[CS-499-04] Demonstrate an ability to use well-founded and innovative techniques, skills, and tools in computing practices for the purpose of implementing computer solutions that deliver value and accomplish industry-specific goals (software engineering/design/database)_

I achieved this in this artifact enhancement by researching and implementing database tools and python libraries to create an interaction between the code I have written and a mysql database. I wrote functions within my project to facilitate this communication. Part of the purpose of my project is to accumulate and store data, so it fits with my artifact that I would have a way to store or backup that data into a database for further manipulation or storage. The CRUD operations I have developed in this artifact mimic is some ways the functionality of a relational database in a simplistic manner. Abstracting to a database seemed like the next logical step for the project. Techniques like this can be used often in production environments to backup or abstract data, and the interaction between functional code that manipulates or uses data and the services in which the data is stored is central to software development.

_4. Reflect on the process of enhancing and/or modifying the artifact. What did you learn as you were creating it and improving it? What challenges did you face?_

My last two enhancements demonstrated my ability to code, and in this enhancement, I demonstrated my knowledge of database principles and mysql syntax. In the process of creating this enhancement, I learned a lot about how to analyze and survey an existing project and consider how to integrate new features and services into it. A large part of this enhancement was thinking of how to integrate this functionality smoothly. During this enhancement, I had to do some research into mysql and python interaction, and faced a few challenges with the data structure. There are some further enhancements I could make, but I think the project is in a good place. If I were to work on this further, I would probably convert the project to just be a light mysql wrapper and ignore the file encryption and json writing, but for now I think it works as a good backup storage system.

### Demo
[![Demo](http://img.youtube.com/vi/wJY2uM3vFR8/0.jpg)](http://www.youtube.com/watch?v=wJY2uM3vFR8  "CS499 Capstone Project Demo")
