
Azure Virtual Machine Hosting and Blob Storage Integration

Introduction
This project demonstrates how to host a static HTML website using Microsoft Azure Virtual Machine and integrate Azure Blob Storage for storing and displaying files online. The project was completed using Ubuntu Server, Apache Web Server, and Azure Blob Storage service.
Objectives

Create an Azure Virtual Machine
Connect to the VM using SSH
Install Apache Web Server
Host a static HTML webpage
Create Azure Blob Storage
Upload files to Blob Storage
Connect Blob Storage files with the hosted website

Technologies Used
Microsoft Azure
Azure Virtual Machine
Ubuntu Server 24.04
Apache2 Web Server
Azure Blob Storage
HTML
PuTTY and PuTTYgen

Step 1 - Creating the Azure Virtual Machine
First, an Azure Virtual Machine was created using the Azure Portal.
VM Configuration
Operating System: Ubuntu Server 24.04
Authentication Type: SSH Public Key
Size: Standard_B2ats_v2
Region: Central India

After deployment, the VM public IP address was generated successfully.

Step 2 - Connecting to the Virtual Machine
PuTTY and PuTTYgen were used to generate SSH keys and connect securely to the Ubuntu Virtual Machine.
SSH Connection
Generated public and private keys
Public key added during VM creation
Connected using PuTTY with .ppk private key

Step 3 - Installing Apache Web Server
Apache Web Server was installed using the following commands:
sudo apt update
sudo apt install apache2
The Apache service was started and verified successfully.


Step 4 - Hosting the HTML Website
The default HTML file was modified inside the /var/www/html/ directory.
Sample HTML Code

<html>
<head>
<title>Azure Cloud Project</title>
</head>
<body>
<h1>Welcome to My Azure Website</h1>
<p>This website is hosted using Azure Virtual Machine.</p>
<h2>Image from Azure Blob Storage</h2>
<img src="https://swt41042rhn.blob.core.windows.net/myfiles/image.jpg" width="400">
</body>
</html>
The website was accessed using the VM public IP address.
Website Output

Step 5 - Creating Azure Blob Storage
An Azure Storage Account was created to store files and images.
Configuration
Storage Account Type: Standard
Redundancy: LRS
Container Access Level: Blob (Anonymous Read Access).

Containers

Step 6 - Uploading Files to Blob Storage
An image file was uploaded to the Blob container successfully.
After uploading, the Blob URL was generated and tested in the browser.
Example Blob URL
https://yourstorage.blob.core.windows.net/myfiles/image.jpg
URL


Step 7 - Integrating Blob Storage with Website
The Blob image URL was added to the HTML webpage using the <img> tag.
As a result, the image stored in Azure Blob Storage was displayed directly on the website hosted in the Azure VM.
Final Output
The final solution successfully demonstrated:
Website hosting using Azure Virtual Machine
Apache Web Server configuration
Azure Blob Storage file hosting
Integration between Blob Storage and hosted website

Final Website Access
http://98.70.28.41

Conclusion
This project successfully implemented cloud-based web hosting using Microsoft Azure services. Azure Virtual Machine was used for hosting the website, while Azure Blob Storage was used for storing and sharing files online. The integration between the VM-hosted website and Blob Storage was completed successfully.

References
Microsoft Azure Documentation
Apache Web Server Documentation
Ubuntu Server Documentation
