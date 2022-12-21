# More Useful Commands

Shows connected status to peers over wireguard VPN: <mark style="background-color:blue;">**`sudo wg show`**</mark>

To bring down and up wireguard:  <mark style="background-color:blue;">`wg-quick down wg0 && wg-quick up wg0`</mark>

Shows IPFS peers. If empty, no one is connected: _<mark style="background-color:blue;">ipfs swarm peers</mark>_

### Logfiles are in:&#x20;

`~/.pm2/logs/outpost-worker-error.log`

`~/.pm2/logs/outpost-worker-output.log`

`/var/log/nginx/`

`ipfs log tail`

## _Typical Storage Node migration_

### Save old .env

### Stop node:&#x20;

`cd ~/dstor-storage-node/ pm2 stop ecosystem.config.js ###Install dependencies git pull npm install`

### Update your .env file

Use .env.example as an example. Variables `NODE_PEER_ALLOWED_IPS, NODE_PEER_LISTEN_PORT, NODE_PEER_PERSISTENT_KEEPALIVE, NODE_PEER_PRIVATE_KEY` might stay empty for default behaviour.

### Restart node&#x20;

`pm2 restart ecosystem.config.js --update-env`\
``Update nginx config for node if any changes

### IPFS swarm

1. After node is automatically set up, check for swarm peers
2. If you see a message, saying something about your node not being online and you don't see an api (no extension at all) file inside your IPFS folder (/ipfs/ probably), make sure you've added `IPFS_PATH env` variable to `.bashrc` and `.profile` and reboot your server.

ipfs swarm peers
