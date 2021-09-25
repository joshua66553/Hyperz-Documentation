# How to update to NodeJS V16+

First off, we have to update ubuntu.
```css
sudo apt update
sudo apt upgrade
```

Next, we need to install the **curl** function/command onto our VPS, so may already have this, but just install it anyways, just to be safe.

```css
sudo apt install -y curl
```

Great, now we have to use the **curl** command to get the latest NodeJS install version.

```css
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
```

Then, we need to officially install the new NodeJS Version, do this by running:

```css
sudo apt install -y nodejs
```

---

# NodeJS Version Checking

Then, check your NodeJS Version with:

```css
node -v
```
