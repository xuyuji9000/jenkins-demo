# jenkins-playground

## Step 0: Prerequisite

    - AWS account
    
    - Domain name

    Dependencies to be prepared before the workshop,[REF](https://github.com/coderbunker/aws-playground/tree/master/Workshop-0-Prerequisite)

## Step 1: Prepare Jenkins 

1. Prepare an EC2 instance 

    - Use **Ubuntu 18.04** 

    - Use default ssh key

    - Command to login: `ssh ubuntu@PUBLIC_IP`

    - Enable the **8080** port 

2. Prepare Jenkins

    A. Install Java

        ```
        sudo apt update
        sudo apt install openjdk-8-jdk
        ```

    B. Install repository 

        ```
        wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
        sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
        sudo apt update
        sudo apt install jenkins
        ```

    C. Start Jenkins

        ```
        sudo systemctl start jenkins
        sudo systemctl status jenkins
        ```
    
3. Configure Jenkins

    A. Access Jenkins from **PUBLIC_IP:8080**

    B. Get the token for login

        ```
        sudo cat /var/lib/jenkins/secrets/initialAdminPassword
        ```    

    C. Choose **Install suggested plugins**

    D. Create admin user




4. Fix creating Jenkins Job page keeps loading problem, with installing [Warnings Plugin](https://wiki.jenkins.io/display/JENKINS/Warnings+Plugin)

5. Jenkins job Github credential could only be added at the beginning of job creation.



## Step 3: Deploy to S3



# Reference 

1. [Install Jenkins on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-jenkins-on-ubuntu-18-04)

2. [How To Install Java with `apt` on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-on-ubuntu-18-04#installing-specific-versions-of-openjdk)
