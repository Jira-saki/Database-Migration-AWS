# Create a Replication instance in DMS
- Create database 

- Replication instance configuration section,

    - Name  : myreplicationinstance

    - Description    : Replicate EC2-Mysql to RDS 

    - Instance class     :  dms.t2.micro ** check Include previous-generation instance classes.**


    - Engine version               : Default

    - Allocated storage (GB)   : 10 GB

    - VPC                         : default VPC

    - Multi AZ      :  Dev or test workload (Single-AZ)

    - Publicly accessible          : Check

- In Advanced security and network configuration section,

    - Replication subnet group  : Default

    - Availability zone                  : Default

    - VPC security group(s)        : Migration-SG

    - KMS master key                  : Default

- Create button to create the replication instance.

- Memo the private & public IP address of the replication instance


# Configure Replication Instance details in Source EC2 Instance
- SSH back into the Source EC2 instance. 

    - Switch to root user: 

            sudo su

    - Login to the MySQL:

            mysql -u root -p

    - Press [Enter]

    - Enter password
    
            source123

    - Press [Enter?]

- Grant root access to the replication instance to connect with the MySQL server on Source EC2. 



        GRANT ALL ON *.* TO root@'<<Private IP of Replication Instance>>' IDENTIFIED BY 'your-root-password';


- Repeat the same step now with the Public Ip address of the replication instance.

        GRANT ALL ON *.* TO root@'3.224.227.68' IDENTIFIED BY 'source123';

- Save the changes by using the following command:

        FLUSH PRIVILEGES;

- Enter exit; to Exit MySQL 

- Restart the MySQL server.

        /etc/init.d/mysql restart

### Replication instance has access for Source Instance MySQL Database.

