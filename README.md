01. Copy the project seperately
02.  Delete all unusual things from your project like .idea folder and other.
03.  check for the version of git ---> git --version
04.  type 'heroku login' in cmd
05.  Go to the folder where u have copied your project in cmd
06.  Create a virtual environment inside the above location using command ---->  'virtualenv .'
07.  activate virtualenv by ----> .\Scripts\activate
08.  Go inside the project folder and run the server if it is showing activation error then go to your pycharm and type ---> 'pip freeze' to see the installed packages.
09. 	  install all the required package inside the project folder  virtual folder using pip command.
10.  Again run the server. if it runs successfully stop the server.
11.  Make a file named 'Procfile' in the folder where manage.py file ia available
12.  write 'web: gunicorn myprojectname.wsgi' in the Procfile
13.  install gunicorn , django-heroku (For New user)
14.  Edit the settings.py file by --> import django_heroku
15. 			      --> django_heroku.settings(locals())	
16.  run 'pip freeze > requirements.txt' in cmd
17.  run 'heroku create webapp-name' in cmd to create your  webapp-name
18.  Execute the below command:-- 
19.  	'git init'
20. 	'git status'
21. 	'git add --all' or 'git add . --force'      # if LF warning occurs then run command --> 'git config core.autocrlf'
22. 	'git commit -m "first commit"
23. 	'heroku git:remote -a webapp-name'
24. 	'git push heroku master'
25. 
26. 
27. ---------------------------------------------------------------------------------------------------------------
28. Error: static files error
29. 
30. Solution - heroku config:set DISABLE_COLLECTSTATIC=1
31. ---------------------------------------------------------------------------------------------------------------
32. 
33. 
34. #########**********************************#########################
35. 		For editing of models and other py files
36. #########**********************************#########################
37. 	a.)	heroku run bash
38. 	b.)	ls
39. 	c.)	python manage.py migrate
40. 	d.)	python manage.py makemigrations
41. 	e.)	python manage.py createsuperuser
42. 	f.)	exit
43. 
44. 
45. 
46. 
47. #########**********************************#########################
48. 		For templates editing 
49. #########**********************************#########################
50. 
51. 	a.)	git status
52. 	b.)	git add --all
53. 	c.)	git commit -m "Thank you page edited"
54. 	d.)	git push heroku master
     
