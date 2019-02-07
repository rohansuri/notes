
### Abstract

* IPFS is a P2P distributed file system

* It models the data as a Merkle DAG which provides an infrastructure to build a versioned file system, blockchain and the permanent web upon.

* It combines the use of DHTs, incentivized block exchanges, self certifying namespaces.


### Introduction

* Aim of IPFS is to be a global distributed file system that is efficient in file distribution.

* BitTorrent is efficient and successful in file distribution, but wasn't created as an infrastructure piece to build upon.

* HTTP is the most successful "distributed system of files" ever deployed. It is the most adopted too, thanks to web browsers. 

  Caveat is it works well only for moving small files around.

* Use cases to handle "lots of data, accessible everywhere" have arised with Big Data computation, on-demand media streaming, etc.

* The aim is to make newer data distribution protocols part of the Web itself.

* Git heavily influences the design for them by offering a content addressed Merkle DAG data model.

### Addendum

#### Merkle DAG

* DAG as we know is a directed acyclic graph.

* Trees are DAGs with a restriction that a node can have only one parent.

* Also called merkle-web, merkle-forest, merkle-chain.

##### Git

* Git's data model is a Merkle DAG too, with nodes being git objects (blobs, trees, commits, tags)

* The directed links that are formed:  
  trees -> blobs  
  commits -> trees

* The reason it's called a *Merkle* DAG is because the links between nodes of the graph are formed by the source node keeping a hash of the content of the target node, which is akin to Merkle trees.

* Essentially the idea being to look up nodes in the graph by their content's hash.

* We use cryptographic hashes to content address since those are the only succinct and unique (high collision resitant) representations of the node.

* Therefore, Git is a content addressable file system.



#### Sybil attacks


