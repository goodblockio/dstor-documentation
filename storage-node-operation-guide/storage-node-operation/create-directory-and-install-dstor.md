# Create Directory & Install dStor

### Create your IPFS Directory Manually

Best practice dictates that this directory should be on a file system that is separate from your OS. For example:&#x20;

`mkdir /ipfs mount /dev/[device array] /ipfs chown -R username`

### Install dstor-storage-node

Clone the git repo in your choice dStor directory, for example: /home/dstor

git clone https://github.com/goodblockio/dstor-storage-node cd dstor-storage-node

Editpre-reqs.sh and setup.sh to your needs. Fill out the IPFS directory, and read the comments.

&#x20;`source ./pre-reqs.sh`

Edit server\_name "nodename.dstor.cloud;" inside storagenode.nginx AND inside setup.sh to your node name. This will set up port openings, nginx config, certbot, ipfs and wireguard. Then Run:&#x20;

`./setup.sh`

Use .env.example file to create your own .env file. If you have questions about the .env values, you can always ask our support team for help.&#x20;

`cp .env.example .env`

To Start the node server: run <mark style="background-color:blue;">`pm2 restart ecosystem.config.js`</mark> from <mark style="background-color:blue;">`dstor-storage-node folder`</mark>` ```&#x20;

To see logs use <mark style="background-color:blue;">`pm2 logs`</mark>&#x20;

To restart the node server: <mark style="background-color:blue;">`run pm2 restart ecosystem.config.js --update-env`</mark> from <mark style="background-color:blue;">`dstor-storage-node`</mark> folder
