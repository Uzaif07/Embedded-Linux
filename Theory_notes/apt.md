# apt notes

You might already know that Ubuntu is derived from Debian Linux.

Debian uses dpkg packaging system.

A packaging system is a way to provide programs and applications for installation

APT (Advanced Package Tool) is the command line tool to interact with the packaging system. 

There is already dpkg commands to manage it. 

But APT is a more friendly way to handle packaging. You can use it to find and install new packages, upgrade packages, remove the packages etc.

-----------------------------------------------------------------------------------------------

Update package database with apt

    cat /etc/apt/sources/list 		//source list of packages

    sudo apt update

    Upgrade installed packages with apt

    sudo apt upgrade

    update vs upgrade

For example, if you have XYZ package version 1.3 installed, after apt update, the database will be aware that a newer version 1.4 is available.  When you do an apt upgrade after apt update, it upgrades (or updates, whichever term you prefer) the installed packages to the newer version.

-----------------------------------------------------------------------------------------------

most convenient way:

    sudo apt update && sudo apt upgrade -y

How to install new packages with apt

    sudo apt install <package_name>

How to install multiple packages with apt?

    sudo apt install <package_1> <package_2> <package_3>


What if you run apt install on an already installed package?

No need to worry. This will just look into the database and if a newer version is found, it will upgrade the installed package to the newer one. So no harm is done by using it, unless you don’t want it to be upgraded.

-----------------------------------------------------------------------------------------------

How to install packages without upgrading?


    sudo apt install <package_name> --no-upgrade


How to only upgrade packages, not install it?

    sudo apt install <package_name> --only-upgrade

How to install a specific version of an application

    sudo apt install <package_name>=<version_number>

-----------------------------------------------------------------------------------------------

How to remove installed packages with apt

    sudo apt remove <package_name>

Another way of uninstalling packages is to use purge. The command is used in the following manner:

    sudo apt purge <package_name>

-----------------------------------------------------------------------------------------------

What is the difference between apt remove and apt purge?

apt remove just removes the binaries of a package. It leaves residue configuration files.

apt purge removes everything related to a package including the configuration files.

-----------------------------------------------------------------------------------------------

Search for packages

    apt search <search term>

See the content of a package

    apt show <package_name>

installed packages on the system 

    apt list --installed


--------------------------------------------------------------------------------------------------

Some other variants

---------------------------------------------------------------------------------------------------

Redhat variant/RHEL (Red hat enterprise linux):
    
    centos  
    package manager 
    yum  #CLI
    .rpm 

openSUSE-based

    SUSE Linux Enterprise Desktop
    package manager
    zypper   #CLI
    yast	#GUI based


-----------------------------------------------------------------------------------------------

&copy;  2022, Rohit Akurdekar&trade;