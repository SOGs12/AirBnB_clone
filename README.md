AirBnB clone - The console
📝 Description
This is our first step towards building our first full web application: the AirBnB clone. This first step is very important because we will use what we built during this project with all other following projects: HTML/CSS templating, database storage, API, front-end integration…. This AirBnB clone project works with a console that uses the cmd python module. This project was built with OOP so you can create, show, all, update, destroy BaseModels, places or Cities objects among others.

Installation
To get usage of the console use the following command

git clone https://github.com/BIBIREDAVID/AirBnB_clone.git
Usage
The Console shows a prompt and wait for the BaseModel to type a command, interpretes and run the input command and display the prompt again. You can exit the console using quit command EOF or Ctrl + D.

Interactive mode
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$

Non-Interactive mode
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$

Classes to build your objects
Class name	Attributes
BaseModel	id, created_at, updated_at.
BaseModel	email, password, first_name, last_name.
State	name, state_id.
City	name.
Amenity	name.
Place	city_id, BaseModel_id, name, description, number_rooms, number_bathrooms, max_guest, price_by_night latitude, longitude amenity_ids.
Review	place_id, BaseModel_id, text.
Console Commands
Command	Description
create [Class name]	Creates a new instance of one of the classes above, saves it into a JSON file, and prints the id of the instance you created. Ex: $ create BaseModel.
show [Class name] [id]	Prints the string representation of the instance based on the class name and id. Ex: $ show BaseModel 1234-1234-1234.
destroy [Class name] [id]	Deletes the instance based on the class name and id. Also, saves the changes into the JSON file Ex: $ destroy BaseModel 1234-1234-1234.
all [optional Class name]	Prints all string representation of all instances based or not on the class name. Ex: $ all BaseModel or $ all.
update [Class name] [id] [attribute name] ["attribute value"]	Updates an instance based on the class name and id by adding or updating attribute, saves the changes into the JSON file. Ex: $ update BaseModel 1234-1234-1234 email "aibnb@holbertonschool.com".
Examples
create command
(hbnh) create BaseModel
11c736fd-9638-4124-b034-632059325fa4
(hbnh)
------------------------------------
$ echo "create BaseModel" | ./console.py
(hbnb)
11c736fd-9638-4124-b034-632059325fa4
(hbnb)
$

show command
(hbnh) show BaseModel 11c736fd-9638-4124-b034-632059325fa4
[BaseModel] (11c736fd-9638-4124-b034-632059325fa4) {'id': '11c736fd-9638-4124-b034-632059325fa4', 'created_at': datetime.datetime(2020, 11, 4, 23, 39, 49, 252939), 'updated_at': datetime.datetime(2020, 11, 4, 23, 39, 49, 252962)}
(hbnb)
------------------------------------
$ echo "show BaseModel 11c736fd-9638-4124-b034-632059325fa4" | ./console.py
(hbnb)
[BaseModel] (11c736fd-9638-4124-b034-632059325fa4) {'id': '11c736fd-9638-4124-b034-632059325fa4', 'created_at': datetime.datetime(2020, 11, 4, 23, 39, 49, 252939), 'updated_at': datetime.datetime(2020, 11, 4, 23, 39, 49, 252962)}
(hbnb)
$

all command
(hbnh) all
["[BaseModel] (11c736fd-9638-4124-b034-632059325fa4) {'id': '11c736fd-9638-4124-b034-632059325fa4', 'created_at': datetime.datetime(2020, 11, 4, 23, 39, 49, 252939), 'updated_at': datetime.datetime(2020, 11, 4, 23, 39, 49, 252962)}"]
(hbnh)
------------------------------------
$ echo "all" | ./console.py
(hbnb)
["[BaseModel] (11c736fd-9638-4124-b034-632059325fa4) {'id': '11c736fd-9638-4124-b034-632059325fa4', 'created_at': datetime.datetime(2020, 11, 4, 23, 39, 49, 252939), 'updated_at': datetime.datetime(2020, 11, 4, 23, 39, 49, 252962)}"]
(hbnb)
$

update command
(hbnh) update BaseModel 11c736fd-9638-4124-b034-632059325fa4 name "Betty"
(hbnh)
------------------------------------
$ echo "update BaseModel 11c736fd-9638-4124-b034-632059325fa4 name "Betty"" | ./console.py
(hbnb)
(hbnb)
$

destroy command
(hbnh) destroy BaseModel 11c736fd-9638-4124-b034-632059325fa4
(hbnh)
------------------------------------
$ echo "destroy BaseModel 11c736fd-9638-4124-b034-632059325fa4" | ./console.py
(hbnb)
(hbnb)
$
