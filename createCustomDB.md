# Create a simple custom Database on Source EC2 Instance

- Create a simple database and create a table inside which will be migrated using DMS.
- SSH to Source EC2 Instance to connect to Source MySQL Client

        mysql -u root -p

Enter Password : source123

- Create a Database

      CREATE DATABASE SchoolDB;


- View the database created

        show databases;



- Switch the database SchoolDB.

        use SchoolDB;



- Create a sample Table of students.

        CREATE TABLE students ( 
        subject_id INT AUTO_INCREMENT,

            subject_name VARCHAR(255) NOT NULL,

            teacher VARCHAR(255),

            start_date DATE,

            lesson TEXT,

            PRIMARY KEY (subject_id));


- See the student table.

        show tables;

- Insert data into the table

        INSERT INTO students(subject_name, teacher) VALUES ('English', 'John Taylor');
        INSERT INTO students(subject_name, teacher) VALUES ('Science', 'Mary Smith');

        INSERT INTO students(subject_name, teacher) VALUES ('Maths', 'Ted Miller');

        INSERT INTO students(subject_name, teacher) VALUES ('Arts', 'Suzan Carpenter');

 
- Check the items added in the Table

        select * from students;

- After database migration, this table can be used as proof of database migration.

## Checking AWS RDS Database before Migration

- Check the databases and tables that exist on the AWS RDS Instance. So that after migration, you will be able to find the new changes. We can use the existing Source EC2 Instance to connect to AWS RDS.

- SSH into the Source EC2 instance. Switch to root user

         sudo su

- Connect to the Amazon RDS Instance 

        mysql -h <RDS Instnace Endpoint> -u <User Name> -p 

Example: mysql -h mydbinstance.c81x4bxxayay.us-east-1.rds.amazonaws.com -u awsrdsuser -p

Enter Password: USEYOURPASSWORD

- After successful login

        Show databases;



- A database by name SchoolDB does not exists now. After migration SchoolDB database will be available here.

