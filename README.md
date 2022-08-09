# Challenge 19 - Cryptocurrency Wallet

For this Challenge, the program "fintech_finder.py" will be written from the perspective of a Fintech Finder customer.  In other words, the User of the program will be able to select a Fintech consultant using the FinTech Finder.  The resultant program will instantiate in a web browser and show 4 choices of consultants.  Contained in the description are the following:

    A. Consultant's Name

    B. A photograph of the consultant

    C. Their Ethereum Account Address

    D. A Fintech Finder Rating (the lowest 1 - 5 the highest)

    E. Their hourly rate quoted in ETH

On the left hand side of the web application, there is additional information provided to the User:

    A. The User's Account Number - in hex format (0xaC8eB8B2ed5C4a0fC41a84Ee4950F417f67029F0)

    B. The User's Account Balance - in ETH

    C. A drop down menu with the four consultant's names for the User to select.

    D. The number of hours that you are seeking to hire the consultant for.

    E. A post-selection Summary of the consultant's name, the total amount of ETH required to hire them, the consultant's Account Address in hex (same as above)

    F. A "Send Transaction" button to execute the transaction, as shown below:  

![Sidebar](sidebar_populated.png)

    G. After the transaction is complete, the Validated Transaction Hash:

![Validated_Trans](validated_trans.png)

    
This program will take the following steps in order to do the following:

    1. Generate a new Ethereum account instance by using the User's mnemonic seed phrase 

    2. Fetch and display the account balance associated with the User's Ethereum account address.

    3. Calculate the total value of an Ethereum transaction, including the gas estimate, that pays a Fintech Finder candidate for their work.

    4. Digitally sign a transaction that pays a Fintech Finder candidate, and send this transaction to the Ganache blockchain.

    5. Review the transaction hash code associated with the validated blockchain transaction.

    6. Once the User receives the transaction’s hash code, the following images will be posted:

        1. Navigate to the Transactions section of Ganache to review the blockchain transaction details. To confirm that you have successfully created the transaction. 

        2. Screenshots will be taken and posted below.  

![Hooray](Hooray!.png)

![Ganache_validation](Ganache_post_trans.png)

![Ganache_trans_confirmation](Ganache_trans_confirm.png)

These final images confirm a transaction was successfully completed.
---

## Technologies

This project leverages python 3.7 employed in a web application called Streamlit, which enables Python code to be displayed in a web site environment.  The following libraries were also imported: 

import streamlit as st
from dataclasses import dataclass
from typing import Any, List
from web3 import Web3
w3 = Web3(Web3.HTTPProvider('HTTP://127.0.0.1:7545'))

Streamlit: https://streamlit.io/

dataclasses: https://docs.python.org/3/library/dataclasses.html

typing: https://docs.python.org/3/library/typing.html

web3: https://web3py.readthedocs.io/

Additionally, the web site Ganache: https://trufflesuite.com/ganache/ was used to test the code and validate the transactions.  This is an important feature as it provides a near real-time environment from which a user can screw up royally and not cost themselves unspeakable amounts of money.  

---

## Installation Guide

The program is meant to be instantiated from the command line to run the "fintech_finder.py" utility.

There is a second program that contains only function critical to the smooth operation of the fintech program.  This program is "crypto_wallet.py" and can be found in the repository for inspection and review.  

A .env file was used to pass the secret mnemonic from which the User's secret key is used to validate transactions.  This is not found in the repository as it contains secret information known only by the user.  

To start the program, navigate from the command line to the where the main program "fintech_finder.py" is found.  From there, type:

    Streamlit run fintech_finder.py

As the program runs and calls Streamlit, a browser will pop up that contains all of the information described above.  


---


## Contributors

The program was largely provided to the author from the Rice University FinTech boot camp program.  The critical code linking all of the items together was done solely by Christopher Todd Garner
---

## License

Feel free to use this program with appropriate references where large code blocks are copied verbatim.  
