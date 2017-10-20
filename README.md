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


# IN DEVELOPMENT!!!