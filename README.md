# marist-mscs621 - Blockchain by Danny Mulick
---
## Introduction
  My application is designed to act as a public ledger for trading card transactions. Each new node that comes into the blockchain network should be able to interact with any of the nodes in the P2P network. This public ledger of card transactions will better help players track where their cards are going, and locate trades they have made 
  
  An instance of this blockchain is already set up on IBM Bluemix at : [https://marist-mcsc621-mulick-blockchain.mybluemix.net/](https://marist-mcsc621-mulick-blockchain.mybluemix.net/)
  
  The system consists of a local API to your version of the blockchain, and a web interface for submitting things to your API and getting information from it. Your API allows you to submit transactions, add connections to other nodes, mine blocks, and resolve your chain among the other nodes in the network that you have added to your list of neighbors.
  
## Deployment
Clone down this repo to the machine you wish to add as a node to the network

Ensure that at least python 3.6.0 is installed on your system. For more information see [here](https://www.python.org/downloads/)

Run ```pip install -r requirements.txt```
After installing all dependencies, either run ```python blockchain.py``` or ```python3 blockchain.py``` to spin up the Flask server on your localhost. Heading to port 8080 on your localhost should show the landing page of the application, and allow you to show the local version of the blockchain.

## Use
The index page allows the user to display the current local chain, mine new blocks to verify transactions, and check the network to see if its local chain is authoritative or if it should obtain the authoritative chain from the network.

The ```/newTransaction``` page allows the user to submit transactions in the form of sender, recipient, and card list requests through the web form. Currently, there is no content control over what can be submitted as a sender or a recipient. In addition, there is only a small set of cards that can be selected from in the web form.

Future expansions on this blockchain would likely include access to either other databases to contain lists of valid cards and users, or dynamically allow insertion of new accepted values as the chain grows.

The ```/addNode``` page exists to allow users to add nodes to the local neighbor array of the current node. Adding neighbors lets the current node poll more versions of the blockchain to determine if its local chain is authoritative. Expected input for this page is ```ipAddress:portNum``` with ipAddress being either a DNS name or the IPv4 address of another node.

Future improvement could be to have chains poll other nodes for extensive connections through the network, creating a true P2P web with 100% connectivity across each node, or research methods of network connection to ensure higher reliability of the network.

## Architecture Diagram
[See here](https://github.com/dannymulick1/marist-mscs621-dannymulick/blob/master/MSCS%20621%20-%20Blockchain%20Diagram.pdf)
