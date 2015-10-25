# provision-racket-ubuntu

Provision a VM to serve as a learning environment for people wanting to learn programming using the book, _How to Design Programs_ (MIT), DrRacket, and MIT AppInventor.

## Steps

From time to time, you will be prompted for an administrator password. Use ```racket```.

Step 1. Create a VM using your favorite virtualization tool (e.g., VMware or VirtualBox).

Step 2. Install a recent version of Ubuntu Linux desktop. Use ```racket``` as the userid and ```racket``` as the administrator password. Apply any available updates.

Step 3. Install git.

```shell
sudo apt-get -y install git
```

Step 4. Clone this repo.

```shell
git clone http://github.com/neopragma/provision-racket-ubuntu
```

Step 5. Run the setup script.

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

Step 6: Manual Firefox configuration

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



