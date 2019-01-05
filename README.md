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


5. Generate your github token, and add to credential

    ![image](https://user-images.githubusercontent.com/4877346/50719539-6c738080-10d8-11e9-9bb7-69c85ca80b3b.png)


## Step 4: Add slave node

1. Create a new instance for slave node

    ```
    sudo apt update
    sudo apt install openjdk-8-jdk
    sudo apt install nodejs
    npm install -g n
    sudo n latest
    sudp apt install awscli
    ```

2. Add slave ssh key to credential

3. Connect Slave Node

## Step 3: Prepare S3 Bucket

1. Create an IAM user

2. Create S3 bucket for static site hosting, [REF](https://github.com/coderbunker/aws-playground/tree/master/Workshop-4-Static-Site-with-S3)

3. Set DNS pointing to the S3 bucket


## Step 4: Deploy website

1. Refer to this [repo](https://github.com/xuyuji9000/jenkins-reactjs)

2. Setup the Github Webhook

# Reference

1. [Install Jenkins on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-jenkins-on-ubuntu-18-04)

2. [How To Install Java with `apt` on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-on-ubuntu-18-04#installing-specific-versions-of-openjdk)
