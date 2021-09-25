**Sometimes** NGINX likes to error out when uploading large images to websites. There is an easy fix to this, simply follow the guide below:

# Step 1

Navigate to your NGINX Config File, it should be something like this: `/etc/nginx/nginx.conf`

![](https://cdn.hyperz.net/qxsybnxz.png)

---

# Step 2

Add the below line to your config file:
`client_max_body_size 10000M;`

Which should lead your config file to look **something** similar to this:

![](https://cdn.hyperz.net/3f824p1q.png)

---

# Step 3

Restart NGINX to enable your changes with this command: `sudo systemctl restart nginx`

![](https://cdn.hyperz.net/1er6yipm.png)
