# Deploy-Django-Project-on-Heroku-Guide

Copy the project seperately
Delete all unusual things from your project like .idea folder and other.
check for the version of git ---> git --version
type 'heroku login' in cmd
Go to the folder where u have copied your project in cmd
Create a virtual environment inside the above location using command ---->  'virtualenv .'
activate virtualenv by ----> .\Scripts\activate
Go inside the project folder and run the server if it is showing activation error then go to your pycharm and type ---> 'pip freeze' to see the installed packages.
  install all the required package inside the project folder  virtual folder using pip command.
Again run the server. if it runs successfully stop the server.
Make a file named 'Procfile' in the folder where manage.py file ia available
write 'web: gunicorn myprojectname.wsgi' in the Procfile
install gunicorn , django-heroku (For New user)
Edit the settings.py file by --> import django_heroku
 			      --> django_heroku.settings(locals())	
run 'pip freeze > requirements.txt' in cmd
run 'heroku create webapp-name' in cmd to create your  webapp-name
	 write- 'git init'
 	'git status'
 	'git add --all' or 'git add . --force'      # if LF warning occurs then run command --> 'git config core.autocrlf'
 	'git commit -m "first commit"
 	'heroku git:remote -a webapp-name'
 	'git push heroku master'

 
---------------------------------------------------------------------------------------------------------------
Error: static files error
 
Solution - heroku config:set DISABLE_COLLECTSTATIC=1
---------------------------------------------------------------------------------------------------------------
 

#########**********************************#########################
 	  	For editing of models and other py files
#########**********************************#########################
a.)	heroku run bash
b.)	ls
c.)	python manage.py migrate
d.)	python manage.py makemigrations
e.)	python manage.py createsuperuser
f.)	exit
 
 
 
 
#########**********************************#########################
 		        For templates editing 
#########**********************************#########################
 
a.)	git status
b.)	git add --all
c.)	git commit -m "Thank you page edited"
d.)	git push heroku master

