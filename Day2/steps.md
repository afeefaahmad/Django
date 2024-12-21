

We have to connect to Mysql Workbench:
step1: 
step2: 
step3:create database called django

![WhatsApp Image 2024-12-21 at 16 41 05_ca78f252](https://github.com/user-attachments/assets/b5c7ae56-30ee-4627-81fb-375d21f09bc1)

Create app named app1
demo> setting.py> Installed_apps> (add new app ie. app1)
Creating tables in app1>models.py









Commands
python manage.py makemigration #To generate  migrations file
python manage.py migrate #To populate with tables
python manage.py runserver

After adding migrations these tables will be visible
![WhatsApp Image 2024-12-21 at 16 34 45_025ce49f](https://github.com/user-attachments/assets/0134e721-1e97-4659-b1ae-48cc330aaa94)

![WhatsApp Image 2024-12-21 at 16 36 20_357770b3](https://github.com/user-attachments/assets/8d1397da-12db-42de-935d-dc1e85954975)

![image](https://github.com/user-attachments/assets/ae4fcf9c-083a-4fba-99ba-a839d56e942b)


Two methods to populate tables with data:
1.Using admin panel    2.Using shell

python manage.py shell
from app1.models import Employee, JobRole, Address, Certifications 
Employee.objects.all().values() 
emprec = Employee.objects.all()
e1 = emprec[0]
e1.ename
e1.age

//Populating Values using shell
e1 = Employee.objects.create(ename="mark", age=24, salary=90000, info="developer ",email="mark@gmail.com", link="https://mark.google.com")
e1.save()
e1.info
e1.age
e1.email

a1 = Address.objects.create(emp_id=e1, address1="velacherry", city="chennai", state="TamilNadu")
a1.save()
a1.address1
a1.city
a1.emp_id.ename   #using foreign key reference
a1.emp_id.info

c1 = Certifications(certificate="intern at hcl", year='2024-11-23')
c1.save()
Employee.objects.all().values()
e1 = Employee.objects.get(id=1)
e2 = Employee.objects.get(id=2)
 c1.emp_id.add(e1, e2)
 c1.save()

 exit() #to exit shell

 python manage.py runserver #re-run the server





