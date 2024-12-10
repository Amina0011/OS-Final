# OS-Final
mini Docker project 

1. Start the docker service and create the folder for the project

   `sudo service docker start`

   `mkdir final `

   `cd final`

3. Download postgres and creating a container 

   `docker pull postgres:latest`

   ` docker run --name uni-db -e POSTGRES_USER=amina -e POSTGRES_PASSWORD=amina -d -p 5432:5432 postgres:latest`

5. checking if the container is running and entering into the container 

   `sudo docker ps`

   `docker exec -it uni-db psql -U amina `

7. creating the tables (one example)

` CREATE TABLE Timetable (
    course_id SERIAL PRIMARY KEY,
    course_name VARCHAR(255),
    day VARCHAR(50),
    time VARCHAR(50),
    room VARCHAR(50),
    level INT
);`  
9. creating and activating the virtual environment
   
      `python -m venv venv`
   
      `source venv/bin/activate`

10. installing the pg8000 and creating necessary files

      `pip install flask pg8000`
   
      `nano app.py`
   
      `mkdir tempaltes`
   
      `touch ./templates/index.html`
   
      `touch ./templates/timetable.html`

12. running the application

      `python app.py`  #inside the final project where app.py  is located

14. accessing the website

      `http://127.0.0.1:5000/`
   



