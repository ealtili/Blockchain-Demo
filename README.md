# Blockchain Demo
A web-based demonstration of blockchain concepts.

This is a very basic visual introduction to the concepts behind a blockchain. 

BlockDemo.py is a simple BlockChain Demo written in Python 3.* 

Class Block defining Block Structure

Class Blockchain defining Blockchain structure and includes adding new blocks, mining chain and blocks. We also check if the chain is broken with checkifbroken function

Class Blockchain Network  comparing blockchain networks.

To run BlockDemo.py open your Python shell and run following comands
# First import everything from Demo by running 
# from Blockdemo.py import * 
# b = BlockChain()
# b.addNewBlock("Hello")
# b.printBlockChain()  /now yo will be able to see hash and signature
# # b.addNewBlock("World")
# b.printBlockChain()
# b.mineChain()
# b.changeData(1, "Hello My World")
# b.printBlockChain()
# b.minechain()

# from block import *
# b1 = BlockChain()
# b2 = BlockChain()
# b3 = BlockChain()
# b1.addNewBlock("Hello")
# b1.addNewBlock("World")
# b1.mineChain()

# b2.addNewBlock("Hello")
# b2.addNewBlock("World")
# b2.mineChain()

# b3.addNewBlock("Hello")
# b3.addNewBlock("World")
# b3.mineChain()

# bcn = BlockChainNetwork()
# bcn.compareBlockChains(b1,b3)



## Setup
Get the code:

```
git clone https://github.com/ealtili/Blockchain-Demo.git
```

Install dependencies:

```
cd blockchain-demo
npm install
```
Run the server:

```
./bin/www
```

Point a web browser at the demo:

```
http://localhost:3000
```

## Setup using Docker

Get the code:

```
git clone https://github.com/ealtili/Blockchain-Demo.git
```

Run the Docker setup:

```
cd blockchain-demo
docker-compose up -d
```

Point a web browser at the demo:

```
http://localhost:3000
```

## Send Thanks
Anders Brownworth, Parth Joshi
