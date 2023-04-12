# Cloud Computing

## DAY 1: Building a Web Application by using AWS services

A simple web-app for calculating the power of a number built by using various **5 different AWS services** like -
**Amplify**, **Lambda**, **IAM**, **API Gateway** and **DynamoDB**.

### AWS Architecture

![aws architecture.](https://github.com/R0-H-1T/Cloud-Computing/blob/main/AWS/First_Web_App/aws-architecture.png)


<hr>

## DAY 2: Hosting a static website on Amazon EC2 instance 


### Choosing an AMI **Amazon Machine Image**:
**Ubuntu Server 20.04(free tier eligible)**

### Hardware configuration:
**Virtual Server Type** - t2 micro (free tier)

### Security Groups:
Inbound Rule
- [x] **default security group config with 22 port open for SSH**
- [x] **HTTP Port 80**
- [x] **HTTPS Port 443**

### Select Key Pair:
**Select/Create a new key pair option – > name your key pair -> Download Key Pair**
Without a key pair u won't be able to SSH into your instance

### LAUNCH 

### EC2 instance configuration -
![ec2 config](https://github.com/R0-H-1T/Cloud-Computing/blob/main/AWS/Hosting_On_Ec2/ec2configuration.png)

### Install Apache2 Server
**Update Packages -> Install Apache2 -> Verify Apache2 is running**
```sh
sudo apt-get update
sudo apt-get install apache2
sudo systemctl status apache2
```
Copy public IP of the EC2 and open in your browser. Apache2 Ubuntu default page appears
**Git is already installed in Ubuntu Server**
So navigating to /var/www/html and cloning 
[https://github.com/R0-H-1T/quickStart] (https://github.com/R0-H-1T/quickStart.git)
```bash
└── html
    ├── index.html
    └── quickStart
        └── DonutsAndCandy
            ├── app.css
            ├── imgs
            │   ├── gumball.png
            │   ├── hand2.png
            │   ├── lolli_icon.png
            │   ├── milk.png
            │   └── sprinkles.png
            └── index.html

4 directories, 8 files
```
### Opening in browser: **(public IP)quickStart/DonutsAndCandy/index.html**

### Start/Restart/Stop Apache Server
```sh
sudo systemctl start apache2
sudo systemctl restart apache2
sudo systemctl stop apache2
```

![ec2 config](https://github.com/R0-H-1T/Cloud-Computing/blob/main/AWS/Hosting_On_Ec2/sampleDonutsNCandy.png)

<hr>