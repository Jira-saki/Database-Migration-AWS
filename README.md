
# Database Migration to AWS project
- Migrate RDBMS (MySQL) to AWS using AWS DMS. 
<img src="https://github.com/Jira-saki/Database-Migration-AWS/blob/main/image/DB-migration.png" width="700">


# Migration Purpose
- Agility of Development and Deployment.
- Improved security in the cloud.
- Save more overhead of local hardware.
- Elastic expansion.
- Improved ability of Cloud Infrastructure.

# Strategies
- Rehosting : Simply Lift and Shift 

- Create simple custom database to simulation realtime database migrate.

# Expections
- Safety perform : no loss of data
- fast to implement : minimum downtime, minimum duplication of infrastructure.
- Securely perform : Security designed in the plan. 




# Used Tools

- I used the tools of this project as follow:
  
    - AWS VPV
    - AWS EC2 (Ubuntu 18.04 lts)
    - AWS DMS
    - AWS RDS (Mysql)
    


## Connect
  - AWS VPC

## Processing
  - AWS management console.
    
  - Create SOURCE Database on EC2 using Ubuntu 18.04 LTS, t2.micro and install Mysql Server.
    
  - Create an AWS RDS instance as DESTINATION Database.

  - At AWS DMS
    - create endpoints for SOURCE Database
    - create endpoints for DESTINATION Database.
    - create a REPLICA Instance
    - create Database Migration Task.
  - Start the Database migration task to replicate the Mysql database on EC2 instance(SOURCE Database) to AWS RDS (DESTINATION Database) 



# Pipelines
- [Create EC2](https://github.com/Jira-saki/Database-Migration-AWS/blob/main/LaunchUbuntuEC2.md) for MySQL Server.
- [Create an Amazon RDS](https://github.com/Jira-saki/Database-Migration-AWS/blob/main/createRDSDb.md) Database.
- [Create REPLICA instance](https://github.com/Jira-saki/Database-Migration-AWS/blob/main/createReplicaInstance.md) in DMS and configure instance details in SOURCE EC2 Instance. 
- [Create endpoints](https://github.com/Jira-saki/Database-Migration-AWS/blob/main/createEndpoints.md) in DMS.
- [Create custom database](https://github.com/Jira-saki/Database-Migration-AWS/blob/main/createCustomDB.md) on SOURCE Database.
- [Create a Database Migration Task](https://github.com/Jira-saki/Database-Migration-AWS/blob/main/createDBMigrationTask.md).


  

# Conclusion
- As hands-on experience on AWS Platform database migration with free tier limitation. I have learn also how to save cost of each service.

- The data pipelines established, i have learn from all the principles of data engineering can carry out rehosting migration process and enable to get securely perform


# Follow Me On
[LinkedIn Profile](https://www.linkedin.com/in/jirasak-pakdeeto-900665214/)

