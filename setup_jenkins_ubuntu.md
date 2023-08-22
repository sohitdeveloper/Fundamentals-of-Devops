# Setting up Jenkins on Ubuntu

This Markdown guide outlines the steps to install and configure Jenkins on an Ubuntu system. Jenkins is a popular automation server used for continuous integration and continuous delivery (CI/CD) purposes.

### Step 1: Update Package Lists
```bash
sudo apt update
```
This command updates the package lists from the repositories to ensure you have the latest information about available packages.

### Step 2: Install OpenJDK 8
```bash
sudo apt install openjdk-8-jdk -y
```
OpenJDK is required to run Jenkins. Here, we're installing OpenJDK 8.

### Step 3: Add Jenkins Repository Key
```bash
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
```
This command fetches the Jenkins repository key and saves it in the keyring for secure package management.

### Step 4: Add Jenkins Repository
```bash
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
```
Here, we're adding the Jenkins repository to the system's package sources.

### Step 5: Update Package Lists Again
```bash
sudo apt-get update
```
After adding the Jenkins repository, update the package lists again to include the newly added repository.

### Step 6: Install Required Packages
```bash
sudo apt-get install fontconfig openjdk-11-jre
```
Install the required packages, including OpenJDK 11 JRE and Fontconfig.

### Step 7: Install Jenkins
```bash
sudo apt-get install jenkins
```
This command installs the Jenkins automation server.

### Step 8: Check Java Version
```bash
java --version
```
Ensure that Java is installed and verify its version to make sure everything is set up correctly.

### Step 9: Start Jenkins Service
```bash
sudo systemctl start jenkins
```
Start the Jenkins service using the systemd init system.

### Step 10: Enable Jenkins Service on Startup
```bash
sudo systemctl enable jenkins
```
Enable the Jenkins service to start automatically whenever the system boots up.

### Step 11: Check Jenkins Service Status
```bash
sudo systemctl status jenkins
```
Check the status of the Jenkins service to ensure it's up and running.

After completing these steps, you should have Jenkins successfully installed and configured on your Ubuntu system. You can access the Jenkins web interface through your browser to start setting up your CI/CD pipelines and automation jobs.

# Now, if you have done ran the commands in AWS EC2 instance (ubuntu) :

Step 11: Configure Security Group (AWS EC2)
When using an AWS EC2 instance, you must modify the security group settings to allow incoming traffic on port 8080, which is the default port for Jenkins.

1. Go to your AWS Management Console.
2. Navigate to the EC2 Dashboard and locate your Jenkins instance.
3. In the "Security groups" section of your instance details, click on the security group associated with your instance.
4. In the "Inbound rules" tab, add a new rule that allows incoming traffic on port 8080 (TCP protocol).
5. You can set the source IP range to "0.0.0.0/0" for testing purposes. For better security, you should limit the source IP range to only the IPs that need access.
After completing these steps, you'll have Jenkins successfully installed and configured on your Ubuntu AWS EC2 instance. You can access the Jenkins web interface through your browser using the instance's public IP address and port 8080. Remember to manage your security group rules to ensure secure access to Jenkins.
