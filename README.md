# CatalogItem-Project
## Description

This repository contains a Web application that queries a database and then dynamically generates complete web pages and API endpoints. Set up to use a virtual machine - Vagrant (VM) to run our database server.

In this project we develop a RESTful web application using the Python framework Flask along with implementing third-party OAuth authentication. Learn when to properly use the various HTTP methods available to you and how these methods relate to CRUD (create, read, update and delete) operations.

## About the Project

Item Catalog
* We use an Object-Relational Mapping (ORM) layer - SQLAlchemy to interact with our database.
* GET and POST requests that translate to CRUD operations.
* Using the Flask framework for development of our application.

We need to be able to successfully run the virtual machine in order to view our projects.

The VM is a Linux server system that runs on top of your own computer.

* We can share files easily between our computer and the VM.
* We'll be running a web service inside the VM which we'll be able to access from our regular browser locally.

We're using tools called Vagrant and VirtualBox to install and manage the VM. You'll need to install these to run the applications.

## Prerequisites
* We'll be using a Unix-style terminal on your computer. On Windows, we recommend using the Git Bash terminal that comes with the Git software (www.git-scm.com).

## Instructions
* VirtualBox is the software that actually runs the virtual machine. Install VirtualBox - (https://www.virtualbox.org/wiki/Downloads).
* Vagrant is the software that configures the VM and lets you share files between your host computer and the VM's filesystem. Install Vagrant - (https://www.vagrantup.com/downloads.html).
* To find out if vagrant has successfully installed type vagrant --version into git bash or cmd


## Configure the VM

* Use Github to fork and clone or download the the repository - https://github.com/udacity/fullstack-nanodegree-vm.
* Once you download the files and end up with a new local directory containing the VM files.
* Change to this directory in your terminal with cd.
* Inside, you will find another directory called vagrant. Change directory to the vagrant directory.

## Start the VM

* Inside the vagrant subdirectory, run the command `vagrant up`
* This will cause Vagrant to download the Linux operating system and install it. This may take quite a while (many minutes) depending on how fast your Internet connection is.
* Once you get your shell prompt back. Run `vagrant ssh` to log in to your newly installed Linux VM

## Creating the SQLite Database.

* once you create a database file, u can create a database by running the following command from within ur project directory inside of the gitbash terminal `python <database_filename.py>` ,in my project it will be `python databse_setup.py`.
* This will create a database file by the name `restaurantmenuwithusers.db`
* Once this .db file has been created inside ur project folder you can populate it by running the following coomand in the gitbash terminal `python lotsfomenus.py` .

## Create a Google ID and client

* Create and then Go to your app's page in the Facebook Developers Console — https://developers.facebook.com/apps/
* Go to Settings from the menu on the left and select Add Product.
* Create Facebook Log in, configure Client OAuth Settings and Valid OAuth redirect URIs (http://localhost:5000) etc and save changes.
* Add your relevant APP ID to the Facebook Log in Script in login.html.
* Set the APP ID and APP Secret in the fb_client_secrets.json file.

## API endpoints

* Show all the restaurant names - `/restaurant/JSON` 
* Show a specific restaurants menu - `/restaurant/<int:restaurant_id>/menu/JSON`
* Show a specific menu item of a specific resaturant - `/restaurant/<int:restaurant_id>/menu/<int:menu_id>/JSON`

## Logging in and out of Vagrant
 
 * If you type exit (or Ctrl-D) at the shell prompt inside the VM, you will be logged out, and put back into your host computer's shell. To log back in, make sure you're in the same directory and type vagrant ssh again.
 * To momentarily stop Vagrant running in the background when done type vagrant halt
 * If you reboot your computer, you will need to run vagrant up to restart the VM.
