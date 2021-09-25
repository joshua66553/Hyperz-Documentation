This default guide uses Ubuntu 20.04 as an operating OS. For windows install please refer to the Windows guides on the side bar.

**Note:** This guide will not work for *all* EJS Based websites, this is designed to work with the basics.

---

# Step 1 - Requirements 

- Server to host the site
- Nginx
- NodeJS
- Domain

# Step 2 - LEMN Stack 

`Props to FAXES for an explanation on this part`

A LEMN stack is a group of programs that will be the core operators for our website.
- **L**inux
- **E**ngine-X (but written as Nginx)
- **M**ySQL Database
- **N**odeJS

You might of heard of a LEMP, or LAMP stack. These include PHP. However, this application uses Node.Js as an handler. So we will use the LEMN Stack.

First off after we login to the terminal. We want to update the package index. then install Nginx.

---

# Actions:

First, lets get logged into our server.
We are going to be using [WinSCP](https://winscp.net/eng/index.php) & [PuTTY](https://www.putty.org/)

Open up PuTTY and input your IP into the Host Name box.

![](https://cdn.hyperz.net/hbvhlyhi.png)

Then when it asks to `login as:` likely your username will be `root`

![](https://cdn.hyperz.net/e1hdets8.png)

If it asks for a password, enter your password. If you don't know your password, reach out to your hosting provider.
Keep in mind the console won't show you as "typing" when entering a password. This is a security feature and it keeps your text entry invisible to other users.

When logged in, you should get **something** like this:

![](https://cdn.hyperz.net/vjgi6rft.png)

### Now onto the next step(s):

Lets make sure we are up to date, so lets run `sudo apt update` in console.

Then let's get to installing NGINX with this command:
`sudo apt install nginx`

When prompted press `Y` to install Nginx.

Now you should be able to navigate to your server IP in a browser and you will see the Nginx welcome page - http://server_domain_or_IP.

# MySQL

If your current EJS website doesn't require a MySQL Database, feel free to skip ahead!

Start off by running this command to install the base of MySQL:
`sudo apt install mysql-server`

When prompted press `Y` to install MySQL-Server.

Then lets install the secure installation below:
`sudo mysql_secure_installation`

It will likely ask you if you wish to remove things, press `Y` for **most** of these.

If you wish to learn MORE about MySQL x Ubuntu feel free to check out the [knowledge base article](https://docs.hyperz.dev/c/knowledgebase/ubuntu20#changing-your-mysql-password-in-linux-ubuntu).

---

# Install NodeJS

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

# Certbot

Lastly we need to install Certbot to be able to use SSL certificates on our domain(s).

for Ubuntu 20:
`sudo apt install certbot python3-certbot-nginx`

for Ubuntu 18:
`sudo apt install certbot python-certbot-nginx`

---

# NGINX Configuration

`Credit to FAXES on this part.`

Because EJS Websites use NodeJS to function we need to setup a proxy to have our website work on a domain through NGINX. Navigate to your NGINX site config: /etc/nginx/sites-available/default

Insert the below into your config file. Ensure to edit the relevant points. If this is your first time editing this file, you may feel free to delete all other content inside of it, so you start blank before pasting this in.

```
server {
    
  server_name example.com; # Change domain to yours.
    
  location / {
    proxy_pass http://localhost:3000; # Change the port if changed in the config file.
    proxy_http_version 1.1;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection 'upgrade';
    proxy_set_header Host $host;
    proxy_cache_bypass $http_upgrade;
    proxy_set_header X-Real-IP $remote_addr;
  }    
}
```

Restart Nginx to make the changes.
`sudo systemctl restart nginx`

---

Now create a SSL certificate through Certbot.

**Ubuntu 20:**
```
sudo add-apt-repository ppa:certbot/certbot
sudo apt install python3-certbot-nginx

sudo certbot --nginx -d example.com
```

**Ubuntu 18:**
```
sudo add-apt-repository ppa:certbot/certbot
sudo apt install python-certbot-nginx

sudo certbot --nginx -d example.com
```

---

When instructed you want to pick the second option `(2)` to redirect all traffic to a https connection.

Run `sudo certbot renew --dry-run` to make sure your SSL certificates auto-renew.
