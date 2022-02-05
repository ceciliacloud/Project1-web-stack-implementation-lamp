# web-stack-implementation

Hello and welcome to the Web Stack Implementation proejct!

What is a Web Stack? It is is a group of software components, used to implement or set up various applications (for example, a website). The "stack" refers to the specific layered components (e.g. OS system, webserver, script interpreter, and database) which are built ontop of each other. One of the most popular web stacks include LAMP, which stands for Linux, Apache, MySQL, and PHP. The LAMP stack will be used for this project! 

## Setting up your virtual enviornment

In order to complete this project, it is necessary to set up a virtual enviornment. In order to achieve this, first, create a free [AWS account](https://aws.amazon.com/)and then create a virtual server using the Ubuntu Server OS. More details to come shortly!

You may be wondering, 'what is AWS'? Amazon Web Services (AWS) is the leading Cloud Service Provider in the world. AWS offers a wide variety of databases and services for different types of applications. This allows users to choose the right tool for the job while receiving the best cost and performance. 

AWS offers a Free Tier for newly registered account users. This enables users to try out some AWS services free of charge within certain usage limits. For this project, I utilized the [EC2 (Elastic Compute Cloud)](https://aws.amazon.com/ec2/features/) compute service, which is covered by the Free Tier!

Let's get started!

Begin by registering and setting up an [AWS account](https://portal.aws.amazon.com/billing/signup#/start) and following the directions on the screen. Once you have created your AWS account, navigate to the login page and type in your credentials.


![](./images/login.png)


Once you have signed-in to your AWS account, navigate to the top-right of the screen and select your preferred region (this region should be the closest area to your physical location).


![](./images/selectregion.png)


After you have selected your region, navigate to the search bar and type in "EC2". Select the EC2 service that appears.


![](./images/selectec2.png)


 Next, click on "Launch Instances".
 

 ![](./images/launchinstances.png)
 
 
  Now we are going to configure our EC2 instance! Select the Ubuntu Server 20.04 LTS (HVM) as the Amazon Machine Image (AMI).
  
  ![](./images/AMI.png)
  

Then, select "t2.micro" as the instance type. Once you have made the selection, click "Review and Launch".

![](./images/instancetype.png)

When you reach the "Review and Launch" page, click the "Launch" at the bottom-right of the page.

![](./images/launchec2.png)

Next, you should see a window appear. Create a keypair and then select "download". Don't lose it! You will need this file in order to connect into your server from your local PC. After you downloaded the key pair, check the box for the acknowledgement, and then click on "Launch Instances".

![](./images/keypair.png)


Great job! You've launched an EC2 instance! You can view your new instance by clicking the "View Instances" button at the bottom-left of your screen. Note: it may take a moment to initalize, so be patient!

![](./images/launchstatus.png)

## Connecting to your EC2 from your local PC

**PLEASE NOTE** - Anchor tags **< >** will be used to indicate contents what must be replaced with your unique values. For example, if you have a file named **"keypair123.pem"** you must enter this information within the corresponding anchor tag: **< private-key-name >**

Now let's connect to our instance! 

Begin by opening Terminal. Once you have opened Terminal, use the `cd` command to change into the directory that your key pair is located. This is usually the `~/Downloads` directory. If you are having difficulty finding it, you can use the `ls` command to list the contents of your current directory.

Once you have located the keypair, use the command below to activate the key file (.pem). This command will also change premissions (otherwise you may get the error “Bad Permissions”). When prompted, enter the password for your PC.

`$ sudo chmod 0400 <private-key-name>.pem`

Next, go back to the AWS console for a moment, and navigate to your running EC2 instance. Copy the Public IP address, as shown in the image below:

![](./images/copyaddress.png)

Now that you've copied the Public IP address, go back to Terminal and connect to the instance by using the command below:

`$ ssh -i <private-key-name>.pem ubuntu@<Public-IP-address>`

Once you entered this command, you will be asked if you want to continue connecting. Type "Yes" and press Enter on your keyboard.

![](./images/loggedin.png)


Nice job! You have successfully connected to your Linux server in the Cloud enviornment! 









Copy and paste the command: `sample code`

![](./images/IMAGENAME.png)

### **Step 1 - ABC...**