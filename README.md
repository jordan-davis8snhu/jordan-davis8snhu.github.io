## Professional Self-Assessment

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

  The artifact I developed during the CS Capstone course demonstrates my software design ability, as well as my understanding of how 
multiple services can communicate and interact with algorithms and data structures. I met the course outcomes of the capstone project 
and demonstrated my ability to meet functional requirements. This artifact works as a ‘password locker’ program, storing and encrypting 
information behind a master password. The program can also store your data in a mysql database. The program is a fully-interactable 
command line program and was written with an end-user in mind. This project demonstrates my ability to research and implement solutions 
to meet requirements and intended outcomes. It shows my ability to build and design functional and reusable code that meets best practices 
and can be collaborated on by any other developer. My code is compartmentalized and abstracted to an appropriate level. I researched 
solutions to the algorithm and database sections of the requirements for the project and implemented them into the program. The three 
enhancements all come together to complete the functionality of the project and all work together with purpose and intention. The three 
enhancements together show my ability as a developer to grasp the different aspects of software development and bring them together into 
one functional project to display my skills.

## Enhancement 1

_Briefly describe the artifact. What is it? When was it created?_

  The original artifact was a project from CS-340 Client/Server Development. The original artifact was a python script that interacted with mongodb through CRUD operations. I took the concept of the CRUD operations and database interaction and expanded on the idea to create something like a password locker. The enhanced artifact is based on the CRUD operations. I have based a new application around them in which the user can store username/password combinations and secure them behind a master password. It functions as a command-line program, which is another enhancement on the original artifact. I created this artifact in the last week as an enhancement of the original project. 

_Justify the inclusion of the artifact in your ePortfolio. Why did you select this item? What specific components of the artifact showcase your skills and abilities in software development? How was the artifact improved?_

  I decided to create and include this project in my ePortfolio because the level of enhancement demonstrates what I have learned about software design in the CS program. The original project was a simple, short script. From that basic functionality I have created a project all of my own with many moving parts and greatly increased functionality. It is a practical, usable program and I have organized it in a professional manner. The artifact also demonstrates my understanding of OOP and modularization of code. Whereas the original project was a single-file script, I now have a full-fledged project that includes multiple directories, function-specific files, a config.py, a master.py and a requirements file. I wrote several classes for this project, containing the appropriate functions, and apply the classes by creating objects and calling the functions. Functions and variables have appropriate and obvious names. Many of the variables are abstracted to the appropriate level and are not hardcoded into the variables themselves. I hardcoded as few things as possible, I think I may have 0 hardcoded values in this project. I have used a config.py and an initialize.py appropriately, which I believe illustrates my understanding of how developers engineer projects to be as modular and configurable as possible. All project-wide variables are configured in the config. This makes the project easily readable and updatable, and the code is easy to follow and understand just by following the workflow through the code. I believe this also benefits the project’s security, since the values are not directly exposed and can be easily updated. Nothing in the code itself exposes the user. Next to all this, I have also successfully converted the project into a command-line application, which can execute a variety of user commands (this is where the CRUD operations come into play). I also did a fair amount of exception handling. I believe this enhancement shows my understanding and ability to apply software design and engineering skills.

_Did you meet the course objectives you planned to meet with this enhancement in Module One? Do you have any updates to your outcome-coverage plans?_

  With this artifact enhancement, I have met or am close to meeting 3 of the course outcomes. In combination with upcoming algorithm/database enhancements, I will meet all of them. The three this artifact accomplishes or begins to accomplish are:
  
_Employ strategies for building collaborative environmentsthat enable diverse audiences to support organizational decision making in the field of computer science_

For many of the reasons stated above. The code is up to standard practices; commented, modularized and abstracted to the appropriate degree, uses a config and standard service organization of directories, files, classes, functions and variables that would be familiar to other developers. Since the program is built to use commands, I have also written a brief readme on how to use the program which I will later expand on. I tried to make the code itself as readable as possible, and others familiar with code would be able to read through it and understand what it is doing and what the workflow through the service is like.

_Demonstrate an ability to use well-founded and innovative techniques, skills, and tools in computing practices for the purpose of implementing computer solutions that deliver value and accomplish industry-specific goals_

With this enhancement I accomplished a robustly designed project that imitates the design/architecture/engineering of what you might see in a real industry service. The service is very modularized and abstracted, and I did a good amount of appropriate exception handling to anticipate service errors or user errors. As far as using innovative skills, techniques and tools, I accomplished this by creating the command-line functionality. I turned the artifact into an executable service that can actually be interacted with from a terminal, and it takes several commands that allow the user to interact with the service in different ways. As far as tools, I have researched and implemented external python libraries to solve complex problems, such as the pyperclip library to directly copy passwords to the clipboard and the cryptography library for data encryption. 

_Develop a security mindset that anticipates adversarial exploits in software architecture and designs to expose potential vulnerabilities, mitigate design flaws, and ensure privacy and enhanced security of data and resources_

While I don’t think this artifact fully accomplishes this outcome, I it beings to address it and demonstrates my understanding of security and securely-designed services. The security of a service really does begin at the design/architecture level. For some of the reasons I have mentioned above, I have begun to touch on this outcome. For instance, the multiple levels of abstraction of variables and the use of a config file. The modularization of functionality. Using the os library to generate paths to files rather than directly exposing the path. Using pyperclip to copy a password to the clipboard when you read it, rather than directly displaying the password on screen. Implementation of a master password to protect the main files where all the other passwords are stored, so that the project has multiple levels of encryption. Hiding the encryption keys in encrypted files themselves rather than storing them inside variables. Then, the encryption itself. While this kind of project would never see real use in the professional world, and while using a fernet algorithm to encrypt text isn’t exactly industry-standard, it illustrates my understanding of a security mindset and mitigating insecure code. For example, you cannot decrypt a file and then quit the program and see the unencrypted data. There is no direct command for decryption, and the file is unencrypted and then re-encrypted with a newly-generated fernet key after each command. This is one example of my consideration of security flaws within the code design.

_Reflect on the process of enhancing and/or modifying the artifact. What did you learn as you were creating it and improving it? What challenges did you face?_	

I learned a lot while creating this enhancement. I was able to apply many of the things I have learned about programming and software design throughout the program. I was able to create a much more complex project than what I started with, just beginning with the CRUD operations. I learned how to use the cryptography library and began thinking with a security mindset, which led to many of my design decisions and greatly influenced how I organized the workflow and execution of the project’s functionality. I also learned the value of abstracting variables and organizing functions into classes, directories and files based on intent and functionality. I designed the project with team collaboration, modularity and configuration in mind, and tried to architect the service in a way that it is very obvious to new developers looking at it.

