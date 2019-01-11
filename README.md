# Procurement-section-implementation-with-Ethereum


            # Procurement-section-implementation-with-Ethereum
                                  
 Aim of project:
                This project ensures the transparency in various transactions that occurs with in procurement process of the university.
                
 Implementation:
                This project is implemented using Ethereum Blockchain technology. Every person shares the immutable ledger of the transactions by connecting peer to peer in the network. This shows the transparency of each and every transaction.
                
Description of project:
 
This project consists of 4 departments:
1.Head of University(HOU usually Vice chancellor)
2.Procurement section(PS)
3.Head of Department
4.Approvers (All department HOD's)

Note: Every department consists of unique address that identifies the transaction of department.
Problem: One of HOD of university requires computers for his department. So has to go through certain process before getting equipment.
The process goes as follows:

1.Intially HOD sends request to PS department seeking computers.
2.PS pushes the received request of HOD to HOU.
3.HOU after getting notified sends notification to Approvers department to verify whether the equipment is really required.
4.Approvers resend notification to HOU by approving or rejecting based on the probabilty of requirement of equipment to department. ( they accept by votings) 
5.If Approvers sends positive feedback then HOU sends his acceptance  to PS deparment.
6.PS deparment goes for tender and sends bill of equipment to HOU.
7.If HOU accepts the amount then Head of the PS department visits HOU with physical bank check document.
8.HOU signes on the check and then PS department releases the fund for bringing equipment.

Note: Every point is a transaction in the above process except 7 and 8. 

This project is implemented in private ethereum blockchain.

Requirements:
Requirement:-
    
      Your pc requires some of modules to run and
      access the smart contract(project) in the ethereum network.

      1.Solc:-
            It is to compile the contract which is written in
            solidity language and returns bytecode and
            Interface.
   
                a.Bytecode:-
                     It is machine understandable code of the
                     contract which is to be deploy into the
                     network.

                b.ABI:-
                     Interface consists of some methods that are
                     there in the contract which can be accessed 
                     by Web3.
       
              
      2.Web3:-
 
            It enables us to deploy and access the contract in
            the ethereum network. 


      3.Mocha:-
 
            This module is for testing the smart contract.


      4.Ganache-cli:-
  
            This module enables you to connect to the local
            network(ganache) for testing smart contract.
    
     5.Truffle HD-wallet provider:-
           
            It establishes a connection between Web3 and
            ethereum.

     6.Metamask:

It is the wallet used to send and receive transactions in the network.




   These project has to completely implemented in ethereum blockchain so that we have to create our own private blockchain.So now we will create a blockchain in the following format.

Step by step process of creating a blockchain
step 1:
     Download Geth: https://geth.ethereum.org/downloads/ 
          Why Geth?
                Geth is used to create a node in the network.

Step 2:
          Download Genesis file: https://github.com/solangegueiros/DevEthereum-Course/blob/master/genesis.json

       Why Genesis?
             Genesis  creates the block in your network.
 Enter the following command in your command prompt as an       administrator.
geth --datadir "C:\ETH\data-private" init "C:\ETH\configs\genesis.json".
Your output will be in following format.

 
Genesis Block  Successfully  created.

Step 3:
lets create your private network.
enter the following command in your cmd.
geth --networkid 1666 --port 60303 --rpc --lightkdf --cache 16 --datadir "C:\ETH\data-private" console.
 it shows output as follows

 

your network has been successfully created with id 1666.


Step 4:
   creation of personal acccount in the network.
      why personal account?
         Personal account is used to mine in the network.
  
enter following command in the cmd to create an account.

personal.newAccount();
your output will be as follows.
 
Your account has been created with the following address.
Use this account address when mining or while doing transactions.

Check if you have balance account:
    eth.getBalance("enter your account address");
          initially  your balance will be 0.000 ether.
          start mining to get the ether.

step 5:
Now lets start the mining.
enter following command to start mining.
Note:-To start mining every time you need unlock your account with following command 
           personal.unlockAccount()

your account is now unlocked start mining by enter the command.

                                  miner.start()
your output seems similar as following
 
 
Use miner.stop() function to stop mining.





    






