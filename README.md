# htb-quickdraw
Small script for quickly setting up a PwnBox for HackTheBox

# Usage:
```bash
git clone https://github.com/thiefadjacent/htb-quickdraw.git ~/htb-quickdraw/
sed -i 's/uname/YOUR_USERNAME_HERE/g' ~/htb-quickdraw/htb.exp
bash ~/htb-quickdraw/htb.exp [pwn ip] [pwn pass] [num ssh tabs] [targ ip] [targ hostname]
```

# Description
This script will automatically copy your local public SSH key to the PwnBox.
It will then open a given number of SSH tabs to the PwnBox, one of which will be a dynamic SSH tunnel for proxying Burp traffic on your local machine through the PwnBox (and to the target box).
The script finally sets DNS records for the target in /etc/hosts.

Accomplishes in 10 seconds what used to take me a few minutes. Skip the boring setup stuff and get right to hacking.
Designed for use on Mac (specifically iTerm2), but will probably work anywhere that has `expect`.
