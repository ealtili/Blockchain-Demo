# Blockchain Demo
A web-based demonstration of blockchain concepts.

This is a very basic visual introduction to the concepts behind a blockchain. 

## BlockDemo.py is a simple BlockChain Demo written in Python 3.* 

Class Block defining Block Structure

Class Blockchain defining Blockchain structure and includes adding new blocks, mining chain and blocks. We also check if the chain is broken with checkifbroken function

Class Blockchain Network  comparing blockchain networks.

To run BlockDemo.py open your Python shell and run following comands

help> BlockDemo
Help on module BlockDemo:

NAME
    BlockDemo

CLASSES
    builtins.object
        Block
        BlockChain
        BlockChainNetwork

    class Block(builtins.object)
     |  Block(no, nonce, data, hashcode, prev)
     |
     |  Methods defined here:
     |
     |  __init__(self, no, nonce, data, hashcode, prev)
     |      Initialize self.  See help(type(self)) for accurate signature.
     |
     |  getStringVal(self)
     |
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |
     |  __dict__
     |      dictionary for instance variables (if defined)
     |
     |  __weakref__
     |      list of weak references to the object (if defined)

    class BlockChain(builtins.object)
     |  Methods defined here:
     |
     |  __init__(self)
     |      Initialize self.  See help(type(self)) for accurate signature.
     |
     |  addNewBlock(self, data)
     |
     |  changeData(self, no, data)
     |
     |  checkChain(self)
     |
     |  checkIfBroken(self)
     |
     |  mineBlock(self, block)
     |
     |  mineChain(self)
     |
     |  printBlockChain(self)
     |
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |
     |  __dict__
     |      dictionary for instance variables (if defined)
     |
     |  __weakref__
     |      list of weak references to the object (if defined)

    class BlockChainNetwork(builtins.object)
     |  Methods defined here:
     |
     |  compareBlockChains(self, bc1, *bchains)
     |
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |
     |  __dict__
     |      dictionary for instance variables (if defined)
     |
     |  __weakref__
     |      list of weak references to the object (if defined)

FILE
    c:\data\blockdemo.py


help> quit

Returning to the Python interpreter.

``` Python
>>> from BlockDemo import *
>>> b = BlockChain()
>>> b.addNewBlock("Hello")
>>> b.printBlockChain()
{0: (0, 0, 'Hello', '185f8db32271fe25f561a6fc938b2e264306ec304eda518007d1764826381969', '0')}
>>> b.addNewBlock("World")
>>> b.printBlockChain()
{0: (0, 0, 'Hello', **'185f8db32271fe25f561a6fc938b2e264306ec304eda518007d1764826381969', '0'), 1: (1, 0, 'World', '78ae647dc5544d227130a0682a51e30bc7777fbb6d8a8f17007463a3ecd1d524', '185f8db32271fe25f561a6fc938b2e264306ec304eda518007d1764826381969')}
>>> b.mineChain()
Mining Block (0, 0, 'Hello', '185f8db32271fe25f561a6fc938b2e264306ec304eda518007d1764826381969', '0')
nonce 24947
new hash 0000cf38af6f0bc77e243c63f177889f2640386adae15e90d048f7ff0cba7692
Mining Block (1, 0, 'World', '78ae647dc5544d227130a0682a51e30bc7777fbb6d8a8f17007463a3ecd1d524', '0000cf38af6f0bc77e243c63f177889f2640386adae15e90d048f7ff0cba7692')
nonce 35146
new hash 00001f1bce3b87d18ce1714fda928c8993bb05a9b839c9e83c2740ccd641699b
>>>
>>> b.changeData(1, "Hello Blockchain World")
>>> b.printBlockChain()
{0: (0, 24947, 'Hello', '0000cf38af6f0bc77e243c63f177889f2640386adae15e90d048f7ff0cba7692', '0'), 1: (1, 35146, 'Hello Blockchain World', 'c46d4260d2ed14e402388ab45c592a46d9371544b68bdea821237679d767a8d6', '0000cf38af6f0bc77e243c63f177889f2640386adae15e90d048f7ff0cba7692')}
>>> b.mineChain()
Mining Block (1, 35146, 'Hello Blockchain World', 'c46d4260d2ed14e402388ab45c592a46d9371544b68bdea821237679d767a8d6', '0000cf38af6f0bc77e243c63f177889f2640386adae15e90d048f7ff0cba7692')
nonce 98449
new hash 00000ff9285ae017d7ca04bf8bf2a843af32a8e6761437729880fbc7f8c0d727
>>>
>>> b1 = BlockChain()
>>> b2 = BlockChain()
>>> b3 = BlockChain()
>>> b1.addNewBlock("Hello")
>>> b1.addNewBlock("World")
>>> b1.mineChain()
Mining Block (0, 0, 'Hello', '185f8db32271fe25f561a6fc938b2e264306ec304eda518007d1764826381969', '0')
nonce 24947
new hash 0000cf38af6f0bc77e243c63f177889f2640386adae15e90d048f7ff0cba7692
Mining Block (1, 0, 'World', '78ae647dc5544d227130a0682a51e30bc7777fbb6d8a8f17007463a3ecd1d524', '0000cf38af6f0bc77e243c63f177889f2640386adae15e90d048f7ff0cba7692')
nonce 35146
new hash 00001f1bce3b87d18ce1714fda928c8993bb05a9b839c9e83c2740ccd641699b
>>> b2.addNewBlock("Hello")
>>> b2.addNewBlock("World")
>>> b2.mineChain()
Mining Block (0, 0, 'Hello', '185f8db32271fe25f561a6fc938b2e264306ec304eda518007d1764826381969', '0')
nonce 24947
new hash 0000cf38af6f0bc77e243c63f177889f2640386adae15e90d048f7ff0cba7692
Mining Block (1, 0, 'World', '78ae647dc5544d227130a0682a51e30bc7777fbb6d8a8f17007463a3ecd1d524', '0000cf38af6f0bc77e243c63f177889f2640386adae15e90d048f7ff0cba7692')
nonce 35146
new hash 00001f1bce3b87d18ce1714fda928c8993bb05a9b839c9e83c2740ccd641699b
>>> b3.addNewBlock("Hello")
>>> b3.addNewBlock("World")
>>> b3.mineChain()
Mining Block (0, 0, 'Hello', '185f8db32271fe25f561a6fc938b2e264306ec304eda518007d1764826381969', '0')
nonce 24947
new hash 0000cf38af6f0bc77e243c63f177889f2640386adae15e90d048f7ff0cba7692
Mining Block (1, 0, 'World', '78ae647dc5544d227130a0682a51e30bc7777fbb6d8a8f17007463a3ecd1d524', '0000cf38af6f0bc77e243c63f177889f2640386adae15e90d048f7ff0cba7692')
nonce 35146
new hash 00001f1bce3b87d18ce1714fda928c8993bb05a9b839c9e83c2740ccd641699b
>>> bcn = BlockChainNetwork()
>>> bcn.compareBlockChains(b1,b3)
>>> bcn.compareBlockChains(b1,b2,b3)
>>> bcn.compareBlockChains(b,b1,b2,b3)
Network is Broken in Chain
Network is Broken in Chain
Network is Broken in Chain
>>> bcn.compareBlockChains(b,b1,b2)
Network is Broken in Chain
Network is Broken in Chain
>>> bcn.compareBlockChains(b1,b2)

```

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

## Thanks
Anders Brownworth, Parth Joshi
