# provision-racket-ubuntu

Provision a VM to serve as a learning environment for people wanting to learn programming using the book, _How to Design Programs_ (MIT), DrRacket, and MIT AppInventor.

## Steps

From time to time, you will be prompted for an administrator password. Use ```racket```.

### Step 1. Create a VM using your favorite virtualization tool (e.g., VMware or VirtualBox).

### Step 2. Install a recent version of Ubuntu Linux desktop. 

Use ```racket``` as the userid and ```racket``` as the administrator password. Apply any available updates.

### Step 3. Install git.

```shell
sudo apt-get -y install git
```

### Step 4. Clone this repo.

```shell
git clone http://github.com/neopragma/provision-racket-ubuntu
```

### Step 5. Run the setup script.

```shell
cd provision-racket-ubuntu
./setup
```

The racket installer will ask you a few questions. Reply as follows.

Do you want a Unix-style distribution?

Reply: no

Where do you want to install the "racket" directory tree?

Reply: 3 (that is, ~/racket)

If you want to install new system links...

Reply: /home/racket

#### Note

Don't worry if you see the following error messages during the racket install:

- /home/racket/share/man/man1 does not exist
- /home/racket/share/applications does not exist

### Step 6: Manual Firefox configuration

To help tailor Firefox to support the intended use of the environment, make the following changes to settings:

```
  General
    Make Firefox the default browser
    When Firefox starts: Show my windows and tabs from last time
  Search
    Duck Duck Go
  Privacy
    Tracking: Tell sites that I do not want to be tracked
    History: 
      Firefox will: Use custom settings for history
      Deselect: Remember my browsing and download history
      Deselect: Remember search and form history
      Accept third-party cookies: Never
      Keep until: I close Firefox
      Select: Clear history when Firefox closes
    Location bar:
      Deselect: History
      Select: Bookmarks
      Select: Open tabs
  Advanced
    General
      Browsing
        Deselect: Check my spelling as I type
    Data Choices
      Deselect: Enable Firefox Health Report
  Privacy (again)
    Select: Always use private browsing mode (requires restart of Firefox)

After restarting, in menu choose
  Tools
    Add-ons
      Install AdBlock Lite
```

## Getting started

The main purpose of this environment is to support beginning programming using _DrRacket_, guided by the book, _How To Design Programs_. 

Firefox is configured to open several tabs, including the help file ```tips-and-hints.html``` on the desktop as well as _How To Design Programs_, the _Racket Language_ homepage, and _Cyber-Dojo_. The _Hints and Tips_ page explains how the environment is set up and how to get started using _DrRacket_ and the _How To Design Programs_ book to learn programming. 

The second learning tool configured in the environment is MIT's _AppInventor_. This is for developing Android applications for smart phones and tablets. You will work with AppInventor online through the site http://appinventor.mit.edu/. MIT provides an Android emulator you can use in lieu of an actual phone, but it is not very easy to configure. This environment has been set up so that you can start and stop the emulator using icons located on the Unity launcher located on the left-hand side of the screen.

