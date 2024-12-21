# altschool_semester2_project
This is my AltSchool Cloud Engineering semester 2 project.\
The following are the required deliverables for this project:
### **Deliverables:**
•	The public IP address or URL of your web page: **35.179.112.244**\
•	A screenshot showing your HTML page in a browser: **Uploaded**\
•	Write clear, step-by-step documentation of how you provisioned the server, installed the web server, deployed the HTML page, and configured networking.\
The following steps were followed in provisioning an Instance, installing a web server, deploying the HTML page and configuring my network:
1.	I launched an Ubuntu LTS EC2 instance from the AWS management console.
2.	Generated a .pem key pair file to enable connection from the CLI. This file was moved to the directory I wanted to work from.
3.	Created a security group, edited the inbound rules to allow SSH traffic on port 22, HTTP on port 80 from 0.0.0.0/0 (for the purpose of this project, I opened up traffic from Anywhere) and connected Instance to security group.
4.	Connected to Instance from CLI using **ssh -i “key pair file” username@instance IP address**
5.	Ran the **sudo apt update** command to update installed packages. 
6.	Checked if any web server has already been installed using the **dpkg -l | grep nginx or nginx -v** to check version for nginx and **dpkg --get-selections | grep Apache or Apache2 -v** to check version for Apache2
7.	Installed Apache2 using command **sudo apt install apache2**
8.	Created a simple HTML page on Visual Studio Code.
9.	Started and checked the status of the Apache webserver using command 
**sudo systemctl start apache2** then **sudo systemctl status apache2**
Then confirmed Apache was installed correctly and working by typing Instance’s public address into a web browser.
10.	Changed directory to /var/www/html to enable copying of the HTML code into the right directory. I removed the Apache default index.html and created a new index.html file using the following command: **rm -r index.html** then **touch index.html**
11.	Copied and pasted HTML code into nano text editor. Open nano editor: **nano index.html** pasted copied HTML code using ctrl+shift+v then write and save. I had to edit file permissions to rwx because I noticed I couldn’t write to file initially.
12.	Copied Instance’s public IP address into web browser to view HTML page.

