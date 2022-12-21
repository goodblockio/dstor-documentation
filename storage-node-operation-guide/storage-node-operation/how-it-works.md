# How it Works



The simplest explaination of dstor-storage-node is that our server sends 'to-be-pinned' messages to the storage nodes to force them downloading every file and folder that should currently be pinned (are present in the database and have hashes).\


Once a day (01:00 UTC) or when a new storage node connects to the server the server runs a task.

1. The server fetches all the hashes of files and folders in the database.
2. Send all of these hashes to the outpost nodes with the 'to-be-pinned' command. If it is run for a newly connected node, this message is sent to this node only, otherwise it is propagated to all nodes.
3. A node receives a hashes list, takes from its IPFS storage all the hashes pinned and makes a comparison.
4. For all missing hashes it runs a code chunk pinning a file to the local ipfs storage (node's one), so the file/folder is recursively downloaded from the server IPFS or from other connected node IPFS storages. As we want to make it as fast as possible, but we don't want the memory to be overflowed, we divide these hashes into chunks (10000 hashes per chunk) and for this chunk we run these pin action asynchronously.
5. Same for hashes that are missing in the list from the server. We delete them from the node's IPFS storage asynchronously.
