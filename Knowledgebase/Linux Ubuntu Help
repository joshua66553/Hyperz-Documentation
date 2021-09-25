# Information

This guide is designed STRICTLY for Ubuntu 20+, older versions may not work with these guides.

These guides are pulled from other sites, and mashed together to help in a more formal and collected webpage, rather than having 18 different tabs open.

If you want to buy a Linux VPS, get one [here](https://snowsidehosting.com/index.php?rp=/store/vps) for **25% OFF** with code `HYPERZ`

Newbies to Linux Ubuntu or MySQL may have some trouble understanding this, just take your time, and read :]

---

# SSH into a Linux Ubuntu Machine.

- Open up a Command Prompt and run this command:

```
ssh root@YOUR-VPS-IP
```

- Enter your provided password you set on your hosting services setup page
- You're done! Welcome to a Linux Terminal!

---

# Use A File Explorer VIA Linux

For this tutorial, I will be using [WinSCP](https://winscp.net/eng/index.php) as it is the more proficient FTP service. You can also use FileZilla if you wish.

- Install [WinSCP](https://winscp.net/eng/index.php)
- Open It
- Enter your Credentials (Hostname/IP, Username, Password)
- Then you can see your Linux Machines Files!

---

# Installing NodeJS V12

Because of the latest package release of NodeJS being weird (It's set to 10 by default) we have to force Ubuntu to install a later version of NodeJS through *commands*! 

Simply open into your Linux Terminal, or into SSH, and run the following commands:

```
sudo apt update
sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -

sudo apt -y install nodejs
```

This forces NodeJS to use V12 instead of V10.

**Q:** Why use V12 instead of V10, and why does it matter?
**A:** It has a huge difference, especially in the Discord side of things, odds are your app won't be Discord Integrated without NodeJS V12 or higher.

---

# MySQL

There is a dedicated article for MySQL
