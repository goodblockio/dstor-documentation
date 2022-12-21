---
description: Create your own user to install and run dStor under.
---

# Create User to Install

<mark style="color:red;">**DO NOT RUN AS ROOT**</mark>

`adduser`` `_`username`_

`usermod -aG sudo`` `_`username`_

`sudo apt update && sudo apt upgrade -y`

* Reboot if needed.

__
