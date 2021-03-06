## Instructions for Windows

### 1. Download and Install VirtualBox

Click <a href="https://www.virtualbox.org/wiki/Downloads" target="_blank">here</a> to go to the <a href="https://www.virtualbox.org/wiki/Downloads" target="_blank">VirtualBox</a>
website. Click on *x86/amd64* to the right of **VirtualBox *x.x.x* for Windows hosts**. Save
the file.

+ Once the installer is downloaded, find the file and double-click it. 
This will open an installation wizard.
+ Run the wizard accepting all the defaults.

### 2. Download and Install Vagrant

Go to the <a href="http://downloads.vagrantup.com/tags/v1.2.7" target="_blank">Vagrant</a>
website and click on *Vagrant-1.2.7.msi*. Save the file.

+ Once the installer is downloaded, find the file and double-click it. 
This will open an installation wizard.
+ Run the wizard accepting all the defaults.

### 3. Download and install the RailsBridge Boston virtual machine

Open a Command Prompt window. You can find the Command Prompt application through 
the Start Menu, All Programs, probably in Accessories.

Type the following command into the window:

```text
vagrant box add railsbridgebos http://66.228.42.213/railsbridgebos.box
```

This will take a while... After it finishes, type the following commands.
Don't worry about what they mean right now. We'll explain soon.

```text
mkdir rbb
cd rbb
vagrant init railsbridgebos
```

You will see the following message:

```text
A `Vagrantfile` has been placed in this directory. You are now
ready to `vagrant up` your first virtual environment! Please read
the comments in the Vagrantfile as well as documentation on
`vagrantup.com` for more information on using Vagrant.
```

That's all there is to installing the Ruby development environment!

Vagrant uses VirtualBox and a virtual machine script to create a *virtual
environment*. A virtual environment is like have another computer inside your 
computer. The script you downloaded and installed tells vagrant how to make a
Linux machine set up for Ruby inside your Windows computer.

### 4. Entering your virtual environment

To enter your virtual environment, type the following commands in a Command Prompt window:

```text
cd rbb
vagrant up
vagrant ssh
```

`vagrant up` starts your virtual environment. It will take a couple minutes and print something like this:

```text
Bringing machine 'default' up with 'virtualbox' provider...
[default] Importing base box 'railsbridgebos'...
[default] Matching MAC address for NAT networking...
[default] Setting the name of the VM...
[default] Clearing any previously set forwarded ports...
[default] Creating shared folders metadata...
[default] Clearing any previously set network interfaces...
[default] Preparing network interfaces based on configuration...
[default] Forwarding ports...
[default] -- 22 => 2222 (adapter 1)
[default] -- 3000 => 3000 (adapter 1)
[default] Booting VM...
[default] Waiting for VM to boot. This can take a few minutes.
[default] VM booted and ready for use!
[default] Mounting shared folders...
[default] -- /vagrant
```

`vagrant ssh` connects you to your virtual environment.
It will print a long welcome message something like this:

```text
Welcome to Ubuntu 12.04 LTS (GNU/Linux 3.2.0-23-generic-pae i686)

 * Documentation:  https://help.ubuntu.com/

Welcome to the Railsbridge Boston virtual machine!

Everything you need for the Suggestotron tutorial is installed, including:

- Ruby 2.0
- Rails 4.0
- sqlite3
- heroku toolbelt
- git

Next steps:

1. Create a SSH key
2. Configure Git
3. Create a Heroku account

The ~/workspace directory from inside the VM shell is identical to the host
directory of your VM workspace.

When you start your Rails app, visit http://localhost:3000 in your web browser.

Last login: Tue Aug 27 00:38:27 2013 from 10.0.2.2
vagrant@precise32:~$ 
```

`vagrant@pricese32:~$` is the command prompt of your Ruby development environment.

Congratulations, you now have the Ruby development environment up and running. Now go forth and do something awesome with it!

[« Back to Installfest](/installfest)

