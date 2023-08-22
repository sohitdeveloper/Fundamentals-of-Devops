```markdown
# Granting Docker Permissions to Jenkins User

This Markdown guide explains how to ensure that the Jenkins user or the user running your Jenkins agent has the necessary permissions to interact with Docker. By granting these permissions, you enable a smooth interaction between Jenkins and Docker for building and deploying containerized applications.

## Step 1: Add User to Docker Group
The most common method to provide Docker access to the Jenkins user is by adding the Jenkins user to the Docker group. This group membership allows the user to interact with the Docker daemon.

On your Ubuntu machine, execute the following commands:

```bash
sudo usermod -aG docker jenkins
sudo service docker restart || sudo systemctl restart docker
```

In the above commands, replace `jenkins` with the actual username that Jenkins is running as. This addition to the Docker group permits the user to execute Docker commands without requiring administrative privileges.

## Step 2: Restart Jenkins
After adding the Jenkins user to the Docker group, it's essential to restart the Jenkins service. This restart ensures that the changes take effect and the Jenkins user can seamlessly communicate with Docker.

```bash
sudo service jenkins restart || sudo systemctl restart jenkins 
```

This step completes the setup, ensuring that the Jenkins user has the necessary permissions to utilize Docker for various container-related tasks.

By following these steps, you enable an environment where Jenkins can efficiently work with Docker, facilitating the CI/CD pipeline by building, testing, and deploying applications within containers.
```
