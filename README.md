# Google Cloud Platform - How-To deploy Shiny Server and RStudio Server
The ultimate guide to deploy Rstudio Open Source and Shiny Server Open Source at Google Cloud Platform

# Introduction
With the advance of cloud computing, and the more acessibility given to this platforms, there's an uprising trend to use the exisiting cloud services, and integrating it with one of the greatest statistical softwares in the market: R!

This guide is a step-by-step way to show how to configure the Google Cloud Platforms as easy as possible, and how to set up two of the most used features of R in the cloud: RStudio Server - To code wherever you are; and Shiny Server, to deploy amazing data visualization websites without worries.

# Setting up the GCP VM instance
In order to use the google services, you need to signup for the cloud feature, with a valid billing account, even though you receive $300 to use the services for the first time.

After logging in with your google account, and setting up your google cloud console. There are a few steps to take that make the experience of using cloud computing easier. First of all, you'll need a few applications to connect to your server, download the desirable autentications to operate and transfer files from the local machine to your google cloud compute engine.

The applications needed are:
- WinSCP: A file transfer feature that allows transition of files from/to your server easily and safely. (https://winscp.net/eng/download.php)
- Putty: The terminal connection that allows the execution of code inside your virtual machine. (http://www.putty.org/)
- Google Cloud SDK: The google service management that allows the import of private keys to your server, and that helps manage firewall rules. (https://cloud.google.com/sdk/docs/quickstart-windows)

## Creating a VM Instance

Since the installation of the desired software is complete, now you need to create your first VM instance. At the sidepanel of Google Cloud Platform's Console, you'll find the Compute Engine menu, and inside that, the VM Instances Option. Clicking on that you'll be prompted to create or import a Virtual Machine. Select Create, and you'll be taken to the following page:

![VM Instance Creation](pics/vm_instance_1.png)

At this section, you can choose a name for your virtual machine, later you can select where that VM instance will be hosted, the cheaper places are in the us, but given the distance, you might find the connection "laggy". After picking the name and the zone, select what kind of instance you'll be holding. This will be given by your use of technologies, if you'll need lots of memory, or lots of processing cores, here's where you'll choose it. The price per month will depend on this configurations.

After choosing the kind of horsepower that will equip your virtual machine, you can choose what kind of Operational System will come installed with it. For this project, I will choose Ubuntu 14.04, that is one of the most stable versions of Ubuntu server, and lots of applications are supported by it. Also, while choosing the OS, you can choose what kind of storage you'll need. For this project we will choose 30 GBs hosted at an SSD. This gives us speed and reliability.

Later, the last thing to do is allow HTTP traffic and create the VM instance. This process might take a while. If all went correctly you probably will see something like this:

![Created VM](pics/vm_instance_2.png)

## Setting up VM connections before installing RStudio or Shiny Server

Now, you have a Virtual Machine hosted at Google Cloud Platform! At the external IP that is given to you, you can access different ports into that server, hosted at the cloud. But before we start installing R, Rstudio Server and Shiny Server, we need to create a secure connection between your local machine and the hosted Virtual Machine.

To do that you click on the arrow, at the left of SSH button, as shown below, and select "View gcloud Command":

![VM SSH authentication](pics/vm_instance_ssh.png)

This step will generate a line of code that will be used to create a secure connection between your local machine, and your server. Do not share this snippet with anyone, since it can be used to connect to your server. Copy this line of code, and paste at the Google SDK app that we downloaded before.

It'll prompt you to authenticate your connection with google, before downloading the private key. After that is done, you'll ve able to find the private key at your Users folder, inside the /.ssh folder. If the authentication went correctly, the gcloud SDK will open a Putty session, running the linux distro that is hosted by the virtual machine, you can close this, since we'll authenticate our connection through WinSCP.

After that is done, you'll open WinSCP, and create a new connection. At the Host you'll insert the EXTERNAL IP ADDRESS that is given by google to your server, the door will remain 22, and the user will be the name of your google account user. After filling this parts, leave the password blank, and click in the Advanced... box, right below the password field. Inside of the Advanced Settings, go to SSH > Authentication at the map to your left. At the field that asks for your Private Key File, you'll click browse, and search for the "google_compute_engine.ppk" file that is stored at your User/.ssh folder.

If this setting went sucessfully, you'll be able to see at the left portion of your screen the files of your local machine, and at the right side of your monitor, the files of you virtual machine. Success, we have managed to enter the files at the google cloud server!







# IN DEVELOPMENT!!!