         ___        ______     ____ _                 _  ___  
        / \ \      / / ___|   / ___| | ___  _   _  __| |/ _ \ 
       / _ \ \ /\ / /\___ \  | |   | |/ _ \| | | |/ _` | (_) |
      / ___ \ V  V /  ___) | | |___| | (_) | |_| | (_| |\__, |
     /_/   \_\_/\_/  |____/   \____|_|\___/ \__,_|\__,_|  /_/ 
 ----------------------------------------------------------------- 

# About
AWS Cloud9 is a cloud-based integrated development environment (IDE) that lets you write, run, and debug your code with just a browser. It includes a code editor, debugger, and terminal. Cloud9 comes prepackaged with essential tools for popular programming languages, including JavaScript, Python, PHP, and more, so you don’t need to install files or configure your development machine to start new projects. Since your Cloud9 IDE is cloud-based, you can work on your projects from your office, home, or anywhere using an internet-connected machine. Cloud9 also provides a seamless experience for developing serverless applications enabling you to easily define resources, debug, and switch between local and remote execution of serverless applications. With Cloud9, you can quickly share your development environment with your team, enabling you to pair program and track each other's inputs in real time.

# Links
https://aws.amazon.com/cloud9/  
https://docs.aws.amazon.com/cloud9/latest/user-guide/  
https://aws.amazon.com/cloud9/pricing/  
https://ace.c9.io/  

# AWS C9 - Install PowerShell Core 6 on AMI image
Source: https://github.com/PowerShell/PowerShell/blob/master/docker/community/amazonlinux/Dockerfile  
Note: Version numbers (cmd number 5) will need to be adjusted after PowerShell versions get's released.

1. sudo yum install -y curl libunwind libicu libcurl openssl libuuid.x86_64 && yum clean all
2. curl https://packages.microsoft.com/config/rhel/7/prod.repo | sudo tee /etc/yum.repos.d/microsoft.repo
3. wget https://raw.githubusercontent.com/PowerShell/PowerShell/master/docker/InstallTarballPackage.sh /InstallTarballPackage.sh
4. sudo chmod +x InstallTarballPackage.sh
5. sudo ./InstallTarballPackage.sh "6.0.1" "powershell-6.0.1-linux-x64.tar.gz"
6. sudo chmod +x /usr/bin/pwsh
7. sudo rm -f InstallTarballPackage.sh