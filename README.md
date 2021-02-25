# How to Install Anaconda on Ubuntu 20.04

![](https://linuxize.com/post/how-to-install-anaconda-on-ubuntu-20-04/featured_hu6328222a1b257c0c0bce48b438541436_38258_768x0_resize_q75_lanczos.jpg)

> This tutorial will walk you through the installation of Anaconda Python Distribution on Ubuntu 20.04. Anaconda is a popular Python/R data science and machine learning platform.

Anaconda is a popular Python/R data science and machine learning platform, used for large-scale data processing, predictive analytics, and scientific computing.

Anaconda distribution ships with 250 open-source data packages, and more than 7,500 additional packages can be installed from the Anaconda repositories. It also includes the `conda` command-line tool and a desktop graphical user interface called Anaconda Navigator.

This tutorial will walk you through the installation of Anaconda Python Distribution on Ubuntu 20.04.

Installing Anaconda
-------------------

At the time of writing this article, the latest stable version of Anaconda is version 2020.02. Before downloading the installer script, visit the [Downloads page](https://www.anaconda.com/products/individual) and check if there is a new version of Anaconda for Python 3 available for download.

Complete the following steps to install Anaconda on Ubuntu 20.04:

1.  Anaconda Navigator is a QT-based GUI. If you are installing Anaconda on a desktop machine and you want to use the GUI application, install the following packages. Otherwise, skip this step.
    
        sudo apt install libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6
    
2.  Download the Anaconda installation script with your [web browser](https://linuxize.com/post/how-to-install-google-chrome-web-browser-on-ubuntu-20-04/) or [`wget`](https://linuxize.com/post/wget-command-examples/) :
    
        wget -P /tmp https://repo.anaconda.com/archive/Anaconda3-2020.02-Linux-x86_64.sh
    
    The download may take some time depending on your connection speed.
    
3.  This step is optional, but it is recommended to verify the data integrity of the script.
    
    Use the `sha256sum` command to display the script checksum:
    
        sha256sum /tmp/Anaconda3-2020.02-Linux-x86_64.sh
    
    The output should look like this:
    
        2b9f088b2022edb474915d9f69a803d6449d5fdb4c303041f60ac4aefcc208bb  /tmp/Anaconda3-2020.02-Linux-x86_64.sh
    
    Make sure the hash printed from the command above matches the one available at the [Anaconda with Python 3 on 64-bit Linux page](https://docs.anaconda.com/anaconda/install/hashes/lin-3-64/) for your appropriate Anaconda version.
    
        https://docs.anaconda.com/anaconda/install/hashes/Anaconda3-2020.02-Linux-x86_64.sh-hash/
    
4.  Run the script to start the installation process:
    
        bash /tmp/Anaconda3-2020.02-Linux-x86_64.sh
    
    You should see an output like the following:
    
        Welcome to Anaconda3 2020.02
        
        In order to continue the installation process, please review the license
        agreement.
        Please, press ENTER to continue
        >>> 
    
    Press `ENTER` to continue. To scroll through the license, use the `ENTER` key. Once you’re done reviewing the license, you’ll be asked to approve the license terms:
    
        Do you approve the license terms? [yes|no]
    
    Type `yes` to accept the license, and you’ll be prompted to choose the installation location:
    
        Anaconda3 will now be installed into this location:
        /home/linuxize/anaconda3
        
            - Press ENTER to confirm the location
            - Press CTRL-C to abort the installation
            - Or specify a different location below
    
    The default location should be fine for most users. Press `ENTER` to confirm the location.
    
    The installation may take some time, and once completed, the script will ask you whether you want to run `conda init`. Type `yes`.
    
        Installation finished.
        Do you wish the installer to initialize Anaconda3
        by running conda init? [yes|no]
    
    This will add the command-line tool `conda` to your system’s [`PATH`](https://linuxize.com/post/how-to-add-directory-to-path-in-linux/) .
    
    To activate the Anaconda installation, you can either close and re-open your shell or load the new `PATH` environment variable into the current shell session by typing:
    
        source ~/.bashrc
    
    To verify the installation type `conda` in your terminal.
    

That’s it! You have successfully installed Anaconda on your Ubuntu machine, and you can start using it.

If you installed Anaconda on a Desktop system, open the Navigator GUI by entering `anaconda-navigator` in your terminal:

Updating Anaconda
-----------------

Updating the Anaconda is a pretty straight forward process. Open your terminal and enter:

    conda update --all

If there are updates, `conda` will display a list and prompt you to confirm the update:

    The following packages will be UPDATED:
    
      anaconda-navigator                          1.9.12-py37_0 --> 1.9.12-py37_1
      conda                                        4.8.2-py37_0 --> 4.8.3-py37_0
      conda-package-han~                   1.6.0-py37h7b6447c_0 --> 1.6.1-py37h7b6447c_0
    
    
    Proceed ([y]/n)? 
    

It is a good idea to update your Anaconda installation regularly.

If you have some trouble erro like:

```bash
Cannot find command
```

then troubleshoot:

    export PATH=~/anaconda3/bin:$PATH



Uninstalling Anaconda
---------------------

If you want to uninstall Anaconda from your Ubuntu system, [remove](https://linuxize.com/post/rm-command-in-linux/) the Anaconda installation directory and all other files that have been created during the installation:

    rm -rf ~/anaconda3 ~/.condarc ~/.conda ~/.continuum

Open the [`~/.bashrc`](https://linuxize.com/post/bashrc-vs-bash-profile/) file and remove the Anaconda directory from the `PATH` environment variable:

~/.bashrc

    # >>> conda initialize >>>
    # !! Contents within this block are managed by 'conda init' !!
    __conda_setup="$('/home/linuxize/anaconda3/bin/conda' 'shell.bash' 'hook' 2> /dev/null)"
    if [ $? -eq 0 ]; then
        eval "$__conda_setup"
    else
        if [ -f "/home/linuxize/anaconda3/etc/profile.d/conda.sh" ]; then
            . "/home/linuxize/anaconda3/etc/profile.d/conda.sh"
        else
            export PATH="/home/linuxize/anaconda3/bin:$PATH"
        fi
    fi
    unset __conda_setup
    # <<< conda initialize <<<

Conclusion
----------

We’ve shown you how to install Anaconda on Ubuntu 20.04. You should now check the official [Getting started with conda](https://conda.io/docs/user-guide/getting-started.html) guide.

If you hit a problem or have feedback, leave a comment below.


[Source](https://linuxize.com/post/how-to-install-anaconda-on-ubuntu-20-04/)



# Part 2.0

# How To Install PostgreSQL on Ubuntu 20.04 [Quickstart] | DigitalOcean

![](https://www.quest.com/community/cfs-filesystemfile/__key/communityserver-components-secureimagefileviewer/communityserver-blogs-components-weblogfiles-00-00-00-00-39/Slide2.JPG_2D00_1100x500x2.jpg?_=637219525519183603)

> PostgreSQL, or Postgres, is a relational database management system that provides an implementation of the SQL querying language. This quickstart guide demonstrates how to install Postgres on an Ubuntu 20.04 server. It also provides instructions for g

### Introduction

[PostgreSQL](https://www.postgresql.org/), or Postgres, is a relational database management system that provides an implementation of the [SQL](https://en.wikipedia.org/wiki/SQL) querying language. It’s standards-compliant and has many advanced features like reliable transactions and concurrency without read locks.

This guide demonstrates how to quickly get Postgres up and running on an Ubuntu 20.04 server, from installing PostgreSQL to setting up a new user and database. If you’d prefer a more in-depth tutorial on installing and managing a PostgreSQL database, see [How To Install and Use PostgreSQL on Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-20-04).

Prerequisites
-------------

To follow along with this tutorial, you will need one Ubuntu 20.04 server that has been configured by following our [Initial Server Setup for Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-20-04) guide. After completing this prerequisite tutorial, your server should have a non-**root** user with sudo permissions and a basic firewall.

Step 1 — Installing PostgreSQL
------------------------------

To install PostgreSQL, first refresh your server’s local package index:

	sudo apt update

Then, install the Postgres package along with a `-contrib` package that adds some additional utilities and functionality:
	
	sudo apt install postgresql postgresql-contrib

Step 2 — Using PostgreSQL Roles and Databases
---------------------------------------------

By default, Postgres uses a concept called “roles” to handle authentication and authorization. These are, in some ways, similar to regular Unix-style users and groups.

Upon installation, Postgres is set up to use _ident_ authentication, meaning that it associates Postgres roles with a matching Unix/Linux system account. If a role exists within Postgres, a Unix/Linux username with the same name is able to sign in as that role.

The installation procedure created a user account called **postgres** that is associated with the default Postgres role. There are a few ways to utilize this account to access Postgres. One way is to switch over to the **postgres** account on your server by typing:

	sudo -i -u postgres

Then you can access the Postgres prompt by typing:

	psql

This will log you into the PostgreSQL prompt, and from here you are free to interact with the database management system right away.

To exit out of the PostgreSQL prompt, run the following:

	postgres=# \q

This will bring you back to the **postgres** Linux command prompt. To return to your regular system user, run the `exit` command:
	
	postgres@server:~$ exit

Another way to connect to the Postgres prompt is to run the `psql` command as the **postgres** account directly with `sudo`:

	sudo -u postgres psql

This will log you directly into Postgres without the intermediary `bash` shell in between.

Again, you can exit the interactive Postgres session by typing:
	
	postgres=# \q

Step 3 — Creating a New Role
----------------------------

If you are logged in as the **postgres** account, you can create a new role by typing:
	
	postgrest@server:~$ createuser --interactive


If, instead, you prefer to use `sudo` for each command without switching from your normal account, type:

	sudo -u postgres createuser --interactive

Either way, the script will prompt you with some choices and, based on your responses, execute the correct Postgres commands to create a user to your specifications.

    OutputEnter name of role to add: sammy
    Shall the new role be a superuser? (y/n) y
    

Step 4 — Creating a New Database
--------------------------------

Another assumption that the Postgres authentication system makes by default is that for any role used to log in, that role will have a database with the same name which it can access.

This means that if the user you created in the last section is called **sammy**, that role will attempt to connect to a database which is also called “sammy” by default. You can create the appropriate database with the `createdb` command.

If you are logged in as the **postgres** account, you would type something like:

	postgres@server:~$ createdb sammy

If, instead, you prefer to use `sudo` for each command without switching from your normal account, you would type:

	sudo -u postgres createdb sammy

Step 5 — Opening a Postgres Prompt with the New Role
----------------------------------------------------

To log in with `ident` based authentication, you’ll need a Linux user with the same name as your Postgres role and database.

If you don’t have a matching Linux user available, you can create one with the `adduser` command. You will have to do this from your non-**root** account with `sudo` privileges (meaning, not logged in as the **postgres** user):
	
	sudo adduser sammy	

Once this new account is available, you can either switch over and connect to the database by typing:
	sudo -i -u sammy
	psql
Or, you can do this inline:
	sudo -u sammy psql

This command will log you in automatically, assuming that all of the components have been properly configured.

If you want your user to connect to a different database, you can do so by specifying the database like this:

	psql -d postgres

Once logged in, you can get check your current connection information by typing:

    OutputYou are connected to database "sammy" as user "sammy" via socket in "/var/run/postgresql" at port "5432".
    

Conclusion
----------

You are now set up with PostgreSQL on your Ubuntu 20.04 server. If you’d like to learn more about Postgres and how to use it, we encourage you to check out the following guides:

*   [A comparison of relational database management systems](https://www.digitalocean.com/community/tutorials/sqlite-vs-mysql-vs-postgresql-a-comparison-of-relational-database-management-systems)
*   [Practice running queries with SQL](https://www.digitalocean.com/community/tutorials/introduction-to-queries-postgresql)


[Source](https://www.digitalocean.com/community/tutorials/how-to-install-postgresql-on-ubuntu-20-04-quickstart)



# peteralexandercharles/git

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT9oB6jmPaiNkrASSSnNGoJPAs4CRLtRFA7pQ&usqp=CAU)

> Contribute to peteralexandercharles/git development by creating an account on GitHub.

### …or create a new repository on the command line

echo "# git" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M master
git remote add origin https://github.com/peteralexandercharles/git.git
git push -u origin master

### …or push an existing repository from the command line

git remote add origin https://github.com/peteralexandercharles/git.git
git branch -M master
git push -u origin master

### …or import code from another repository

You can initialize this repository with code from a Subversion, Mercurial, or TFS project.

[Import code](chrome-extension://cjedbglnccaioiolemnfhjncicchinao/peteralexandercharles/git/import)

**ProTip!** Use the URL for this page when adding GitHub as a remote.


[Source](https://github.com/peteralexandercharles/git)





