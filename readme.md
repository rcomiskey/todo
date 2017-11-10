<!--To do list using Django-->

<!--Install Django-->
sudo pip3 install django

<!--Start a new project called todo:-->
django-admin startproject todo .

<!--restart terminal-->

<!--type run-->

<!--read secomd line of the error wen opening the app-->
<!--add to allowed hosts as per the yellow error -->
ALLOWED_HOSTS = ["todo-desc.c9users.io"]

<!--stop app running-->
ctrl+C

<!--fix red error in the console-->
python manage.py migrate

<!--open sql lite shell-->
<!--NB to exit if required type .quit-->
sqlite3 db.sqlite3
<!--to see tables-->
.tables
<!--to quit-->
.quit

<!--Create a top level user-->
python3 manage.py createsuperuser
username
email
password

<!--admin account setup - test with the following-->
run
go to the site link
add admin t the end of the urls

<!--admin link is nt hte username of the account it is the general administration page-->
http://todo-desc.c9users.io:8080/admin/

login with the details

<!--quit out to bash prompt-->
ctrl+c

<!--Create new ap-->
python3 manage.py startapp todoitem

class Todoitem(models.model)

<!--update DB-->
python3 manage.py makemigrations
python3 manage.py migrate

url to views

<!--template into view in views.py-->
def get_index(request):
   return render(request, "index.html")
   
data into view

send to display