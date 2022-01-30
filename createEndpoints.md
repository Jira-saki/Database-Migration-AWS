# Create Endpoints in DMS
### Create the Source and Target endpoints for EC2 and RDS Instances. These endpoints will help to connect replication instance with both source and target machines. 


## Source Endpoint
   
    
- Click Create endpoint button.

    - Select endpoint as : Source endpoint

    - Uncheck : Select RDS DB instance: 

- Endpoint configuration:

    - Endpoint identifier     :  sourcemysqlendpoint

    - Descriptive Amazon Resource Name (ARN): sourcemysqlendpoint

    - Source engine           : Select MySQL

    - Access to endpoint database: Choose Provide access information manually

    - Server name               : Public IP address of Source EC2 Instance

    - Port                  :  3306

    - Secure Socket Layer (SSL) mode: None

    - User name                 :  root

    - Password         : source123

- Test endpoint connection:

    - VPC                             : Default

    - Replication instance          : myreplicationinstance 

- Run test to test the connection of “successful” result. 

- Create Endpoint.

### Target Endpoint
- Click on the Create endpoint button.

    - Select endpoint as Target endpoint 

    - check : Select RDS DB instance

    - Select RDS Database: mydbinstance

- Endpoint configuration:

    - Endpoint identifier    :  mydbinstance

    - Descriptive Amazon Resource Name (ARN): awsrdsendpoint

    - Target engine            : MySQL

    - Access to endpoint database: Provide access information manually

    - Server name             : mydbinstance.xxxxxxxxxxxx.us-east-1.rds.amazonaws.com 
    - Port                 :  3306
    - Secure Socket Layer (SSL) mode: None

    - User name         :  awsrdsuser
    - Password               : USEYOURPASSWORD

- Test endpoint connection:

    - VPC                : Default

    - Replication instance          : myreplicationinstance 
- Run test to test the connection.

- Create endpoint.

