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

## Architecture Diagram
To be added later
