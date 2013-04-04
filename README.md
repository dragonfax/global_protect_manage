
Rationale
====

I got sick of installing/reinstalling our VPN every time I wanted to do work from home.
And worse, every time I opened my laptop, as it installed faster than it could unblock my network naturally.


I understand some people get away with using the popular global-on/off aliases making the rounds.
But they never worked for me, and instead just left my DNS and networking broken.


```
alias global-off='sudo mv /Applications/GlobalProtect{,OFF}.app && pkill -9 -f GlobalProtect'
alias global-on='sudo mv /Applications/GlobalProtect{OFF,}.app'
```

So here are some scripts to automate installing, removing, and reintalling Global Protect

Quick Start
====

You'll need to go download the GlobalProtect.pkg from our Confluence, as I can't distribute that publically.
Drop in the directory with the scripts and then the 3 gp_scripts will work.

[Confluence VPN Documentation](https://zendesk.atlassian.net/wiki/display/IT/How+to%3A+Setting+up+Global+Protect+VPN)


Usage
====

I suggest:

When you need to do work.
```
$ gp_install
```

When you're done doing work.
```
$ gp_remove
```

And if your working and you're computer goes to sleep. You may find this reconnects much faster.
```
$ gp_reinstall
```
Which just calls the 2 above scripts in succession.


I do this often, and it doesn't damage my mac.

NOTE: The scripts may ask for your password as they use sudo to do the installation/uninstallation.

