# Always add you app to your installed apps in setting.py


Library management system for Relevel

Problem Description:- 

Create a Django Project which manages the Book Transactions. It will contain User,Bookshelf,No. Of book items etc. Focus on Backend Design, Business logics and REST APIs .

The candidate should ensure the availability of Git, Python and Django on their system as part of the setup exercise.. Preferred IDE is PyCharm to import the project directly. Postman tool to test the REST APIs and git.


Problem Breakdown 

To start the development a skeleton repo for the project is provided at the github link –
https://github.com/kumarram1011/Dec_Q1  (master branch)

Then repo can be cloned into their local system through HTTPs or SSH.  After cloning the project at your location, follow the below points:
	
Create Virtual env (ubuntu)
		1. sudo apt install python3-venv
		2. python3 -m venv relevel_env
		3. cd relevel_env/
		4. source bin/activate
Now quit this env location and jump to your working location/ Parent directory
	 
		
Install all dependencies using ‘pip install -r requirements.txt’
Now run your initial migrations with the command as:
	1. python manage.py makemigrations
	2. python manage.py migrate
	
	Note :- 
A.  Initially there is no any model in your projects so the 1st command  will give you
      the response has "NO changes" but the 2nd command will configure you all initial
      settings like DB and all.
	B.  At every stage while developing/implementing the features please use both of the 
                 above commands to reflect your changes in the running/development server.

Run ‘python manage.py runserver’ to start the development server. 
The hosted app can be checked on http://localhost:8000 on the browser. 





Template 1 :

Assume you are the owner of these tools and you need to create for personal purpose only. So no need for any Admin or staff .

	
	Story 1.
	1. Create a User/Customer app/module to perform user related stuff.
	2. Inherit the Django "AbstractBaseUser" for your user model.
	3. Create a model "user" with basic details as :- First Name, Last Name , Email , Phone , 
                Password . You can add more if needed.
	4. Create an API for SignUp/Register the user with basic details as :- First Name, Last Name , 
                Email , Phone , Password .
	5. Only Admin/You are able to add the customer.
	
	Story 2.
	1. Create a model for the Bookshelf with necessary fields with a unique shelf number.
	2. Design an API for creating a Bookshelf.
	3. Use proper serializer for API response.
	4. For creating User View please use Function Based API Views and for creating Bookshelf
                views please use Function Based API Views.()
	5. Use dummy JWT for user authentication. No need to implement the auth model of Django.





























Template 2 :

You have to create Two types of user as customer and Admin. Where Admin will operate your system.
	
	Story 1.
	. Create a User/Customer app to perform user related stuff.
	2. Inherit the Django "AbstractBaseUser" for your user model.
	3. Create a model "user" with basic details as :- First Name, Last Name , Email , Phone , 
                Password . You can add more if needed.
	4. Create an API for SignUp/Register the user with basic details as :- First Name, Last Name , 
                Email , Phone , Password .
	5. Both types of users can register themselves. (you can use user_type as admin,user with the
      help of Enum).
6.Use dummy JWT for user authentication. No need to implement the auth model of Django.

	Story 2.
1. Create a model for the books with necessary fields.
2. Add one more field as no_of_book for all available copies.
	3. Design an API for adding Book
	4. Use proper serializer for API response.
	5. Design a GET API for fetching all the book details .
	





























Template 3 :
	
	Story 1.
	1. Create a User app/module to perform user related stuff.	
	2. Create a model "user" with basic details as :- First Name, Last Name , Email , Phone , 
                Password . You can add more if needed.

	3. No need to create a user registration/signup. You can create the record in DB as 
(
First Name:- Admin, 								
Last Name:- Test , 								
Email:- TestAdmin@gmail.com , 							 Phone:- *********** ,								
Password:- Admin@123
 ).


	4. Create an API for fetching single user details.
	5.Create an API for updating single user details. Use PATCH and PUT and describe their
    difference and uses in your loom video..
	
	Story 2.
	1. Design the Book model containing the following fields .(Add more if needed)
2. No need to create the API for adding books. You can use this followings data for for:-
	(
Book ID:- “DS/relevel-1/A001”, 							
Book Name:- “Data structure using Python” ,					
Edition:- 3rd, 	
Author:- “Alford”,								
DOP:-  09/12/2009.
No of Copies :- 12
)


(
Book ID:- “C/relevel-1/A001”, 							
Book Name:- “Programming with C” ,					
Edition:- 5th, 	
Author:- “Alford”,								
DOP:-  09/12/2009.
No of Copies :- 2
)
	3. Create an API for issuing a book to the customer.
	4. Use a Primary Key/ManyToMany field in user model for assigning the Book to the
    customer.
		Hint :- issued_book = model.ManytoMnyField(Book, default=[])
	5. While issuing the book update the available copies of that particular book.
	6. Create an API for listing all books with their available copies.















Submission Instructions

Code Submission: 
Compress the code on the local system in the form of a *.zip file.
Upload the code on your personal google drive in a folder titled - “Name_BD_<Round Name> Code Base”
Don’t forget to change the permissions of the folder to ‘Anyone with the link can edit’.



Loom video submission: 
Create an account on Loom. 
Go through the quick tutorial on how to record loom videos. 
Create a Loom video (while screen sharing) covering the following points:
Show the functionality of the app you have created i.e demo of the working APIs through a command line. (1 min)
Run through the key parts of your code explaining the core logic and how you organized the code. (2 min)
Explain your problem-solving approach (what logic you have used and why). (2 min)
Please keep your explanation to under 5 mins only.
Avoid too much jargon and explain your app in a simple and clear manner. 



