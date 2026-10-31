# **PROJECT OVERVIEW**

This project demonstrates the practical use of Burp Suite Community Edition for web application security testing and penetration testing.

Burp Suite is a web application security testing tool developed by PortSwigger. It helps security professionals intercept, inspect, modify, 
and analyze HTTP/HTTPS requests and responses between a browser and a web server.The main objective of this project is to understand how web 
applications communicate with servers, identify potential security vulnerabilities, and perform manual security testing in a controlled lab environment.

# **PROJECT OBJECTIVES**

Understand web application penetration testing.

Install and configure Burp Suite Community Edition.

Configure browser proxy settings.

Intercept and analyze HTTP/HTTPS traffic.

Understand HTTP requests and responses.

Perform manual vulnerability testing.

Identify common web application vulnerabilities.

Understand OWASP Top 10 security risks.

Document security findings and recommendations.

# 1. BURP SUITE INSTALLATION

Step 1: Download Burp Suite

Open the official PortSwigger website.

Visit: https://portswigger.net/burp/communitydownload

Select Burp Suite Community Edition.

Choose the appropriate operating system:

Windows x64

Linux x64

macOS

Download the installer.

# Step 2: Install Burp Suite on Windows

Navigate to the downloaded installer.

Double-click the installer.

Follow the installation wizard.

Accept the license agreement.

Select the installation directory.

Complete the installation.

Launch Burp Suite.

# Step 3: Install Burp Suite on Kali Linux

Download the Linux x64 installer from the official website.

Open the terminal.

Navigate to the Downloads directory.

cd ~/Downloads

Give execution permission to the installer.

chmod +x burpsuite_community_linux_*.sh

Run the installer using its actual downloaded filename.

./burpsuite_community_linux_*.sh

Follow the installation wizard.

Launch Burp Suite from the Applications menu.

# **2. INITIAL CONFIGURATION**

After launching Burp Suite:

Select Temporary Project.

Click Next.

Select Use Burp Defaults.

Click Start Burp.

Burp Suite will open its main dashboard.

<img width="1586" height="845" alt="image" src="https://github.com/user-attachments/assets/0f46009e-a2df-4648-ba25-b606f621acdb" />

# **3. PROXY CONFIGURATION**

Burp Proxy acts as an intermediary between the browser and the web server.

It allows us to intercept and inspect HTTP/HTTPS requests and responses.

# Step 1: Configure Proxy Listener

Open Burp Suite.

Navigate to Proxy → Proxy settings.

Locate Proxy Listeners.

Check whether the default listener is running.

<img width="1600" height="852" alt="image" src="https://github.com/user-attachments/assets/c459aec6-2335-4ca4-a555-1a660b2aa662" />

# Step 2: Configure Browser Proxy

For an external Firefox browser:

Open Firefox.

Navigate to Settings.

Search for Network Settings.

Click Settings.

Select Manual Proxy Configuration.

Enter the following details:

<img width="1600" height="852" alt="image" src="https://github.com/user-attachments/assets/0f4d032e-fc4c-4d17-87d5-16b45515205c" />

Save the settings.

Alternatively, use Burp's built-in browser through:

Proxy → Intercept → Open Browser

The built-in browser is already configured to work with Burp Proxy.

# **4. HTTPS CERTIFICATE CONFIGURATION**

To intercept HTTPS traffic using an external browser, Burp Suite requires its CA certificate to be trusted by that browser.

Steps:

Start Burp Suite.

Make sure the proxy listener is running.

Configure your browser to use Burp Proxy.

Open the browser and visit:

http://burpsuite

# **6. PRACTICAL WEB APPLICATION TESTING**

For practical testing, use a deliberately vulnerable application such as DVWA or OWASP Juice Shop.

# Step 1: Open the Target Application

Start your vulnerable web application in the lab environment.

http://altoro.testfire.net/

<img width="1600" height="852" alt="image" src="https://github.com/user-attachments/assets/99f0ac46-c996-4185-8d5c-5ee751e42dd9" />

# Step 2: Intercept HTTP Requests

Open Burp Suite.

Go to Proxy → Intercept.

Enable Intercept.

Open the target application in Burp's browser.

Perform a login or submit a form.

Observe the intercepted HTTP request.

Analyze request headers, parameters, cookies, and body.

# Step 3: Analyze HTTP Requests

Observe the following components:

HTTP Method (GET, POST)

Request URL

Host Header

User-Agent

Cookie

Parameters

Request Body

# Step 4: Use Burp Repeater

Select an intercepted request.

Right-click the request.

Select Send to Repeater.

Open the Repeater tab.

Modify a test parameter.

Click Send.

Compare the server responses.

<img width="1586" height="845" alt="image" src="https://github.com/user-attachments/assets/f506e390-d844-41f6-8618-5c681f701761" />

# Step 5: Open Burp Suite Intruder

Open Burp Suite.

Start a Temporary Project.

Select Use Burp Defaults.

Open the Proxy tab.

Open your authorized test application (altoro.mutual).

Perform a test action, such as submitting a search form.

Go to Proxy → HTTP history.

Select the HTTP request.

Right-click and select Send to Intruder.

Add word list and password list and start cluser bomb attack if it find the different length then we can detect the user and
password for the given website

<img width="1586" height="845" alt="image" src="https://github.com/user-attachments/assets/6d626e99-543a-44ca-9496-27b71ca75593" />

<img width="1495" height="845" alt="image" src="https://github.com/user-attachments/assets/a517a0cb-c6b6-4c30-a1ef-77ee5b033a97" />

# **CONCLUSION**

This project provides practical knowledge of web application penetration testing using Burp Suite Community Edition.

Through this project, I learned how to install and configure Burp Suite, intercept HTTP/HTTPS traffic, analyze web requests and responses, and perform manual security testing.

I also gained an understanding of common web application vulnerabilities and the importance of identifying and mitigating security risks.









