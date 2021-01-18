# Technical Summary

## Roadmap

### Q1 2021 - Blank V1
- Web extension wallet with Tornado.Cash relayer → using existing Tornado.Cash infrastructure (0.1; 1; 10 and 100 ETH smart contracts with already pooled ETH) to deliver basic privacy functionality within a wallet.
- Referral system → Tracking deposits of referred users and rewarding the referrer in BLNK tokens.
- Public Security Audit → security measures before the release of V1 to ensure safety of funds held on Blank Wallet.

### Q2 2021 - Blank V2
- ERC-20 Support → allowing any ERC-20 token deposits; promoting WBTC pool
- Automatic deposits → funds deposited into any personal Blank Wallet address will automatically be sent into the main Blank pool.
- One time address → each time withdrawing from the main Blank pool would automatically create a new address to withdraw into.
- Proof-of-funds compliance key → choose who you provide your transparency to. Providing a compliance key of specific withdrawn addresses would reveal the origins of the deposit.
-Web 3 compatibility → connect to all DeFi applications.

### Q3 2021
- Blank functionality integration to Metamask snaps PlugIn → while still in Alpha, a full release would allow existing MetaMask users to install additional plugins, such as Blank plugin, to get additional features on their existing MetaMask wallet.
- Tor integration → The relayers, dApp sites or node providers could theoretically track users by the IP address the requests for deposit or withdrawal are coming from and thus connect depositing and withdrawing addresses. To mitigate this, Tor can be used, so the user’s IP cannot be tracked and changes with each action.

### Q4 2021 - Blank V3
- Partial withdrawal → independent ETH pools, no longer based as Tornado.Cash relayers, instead of withdrawing the same amount deposited. 
- Unique pool reward system → anyone can create reward milestones for pooling funds and providing privacy for others.


## How does it Work?

The Blank Wallet V1 functionality is based on Tornado Cash [private transactions](https://tornado-cash.medium.com/introducing-private-transactions-on-ethereum-now-42ee915babe0).

The tornado mixer at [tornado.cash](https://tornado.cash/) is a tool that allows any address to send or mix their Ether or Ethereum tokens in a non-custodial way solely based on strong cryptography.

It uses smart contracts, where the Ether or Tokens can be deposited and then be withdrawn to a different address. There is no way to link the withdrawal to the deposit, ensuring complete privacy. This is accomplished by using **zkSnarks proofs**. 

To make a **deposit**, the user generates a secret and sends the [**Pedersen Hash**](https://iden3-docs.readthedocs.io/en/latest/iden3_repos/research/publications/zkproof-standards-workshop-2/pedersen-hash/pedersen.html#pedersen-hash) of a nullifier and the secret, along with the funds to mix, to the smart contract. This is called a commitment and is accepted by the contract, along with the funds.

A hash function is a **one-way function**, which means that the hash of a secret can be easily calculated, while it is near-impossible to calculate the secret from a given hash. This property is used to guarantee that only a user in possession of the secret to a given commitment can withdraw funds from the contract.

In order to make a **withdrawal**, the user needs to provide proof that they possess a secret to an unspent commitment in the smart contract. [**zkSnark technology**](https://consensys.net/blog/blockchain-development/introduction-to-zk-snarks/) allows to do that, without revealing which deposit corresponds to the secret. In other words, zkSnarks allow users to prove that they own a deposit in the contract, without revealing the exact deposit they know the secret of. The withdrawing address can not be connected to the depositing address in any way.

The so-called **Anonymity Set** shows how many deposits still await for a withdrawal. It is a measurement of anonymity, since the bigger the anonymity set is, the bigger is the scope of addresses that could theoretically be the depositing address for a withdrawing address.

To further increase anonymity and privacy, several measures can be taken. In order to not allow for external viewers to make a connection between depositing addresses and withdrawing addresses, the withdrawal should not be done right after the deposit for example.

Even though existing providers like tornado.cash offer user-friendly interfaces, the whole process can be very time consuming and too technically advanced for the average crypto user. This results in lower usage, a smaller Anonymity Set and in turn lower privacy. Users have to manage their notes, the creation and management of different addresses, and they have to take care of following best practices to preserve privacy, like when to withdraw and to use a different IP-address for each action.

## How is Blank better? 

Blank on the other hand, provides seamless integration with the anonymity pool to create a user-friendly browser extension wallet. Users do not have to write down secret phrases, go through tedious transaction processes or manually create several wallets. The ease of use in the wallet and its privacy features result in more usage, a larger Anonymity Set and, in turn, higher privacy for all users.

Blockchain users are also susceptible to off-chain tracking. Due to node and dapp providers receiving data from users, they can perform extensive tracking by fingerprinting and profiling the users’ requests. Blank goes one step further to provide the maximum amount of privacy while retaining a frictionless user experience. In order to further protect users from tracking, both on-chain and off-chain, Tor is integrated into Blank. This means that sending transactions to node providers or interacting with Dapps can be done over the Tor network, providing the user with complete anonymity.

## Security

Without a doubt, security is an important factor when it comes to building advanced cryptocurrency wallet software. Blank is aware of this, and approaches security with a high level of attention. Additionally, we are also aware that security and privacy go hand in hand - one cannot work without the other.

Using proven and audited technology and best practices is the way to maximize security. The basic infrastructure on Blank is built by integrating already existing solutions and practices that have been proven over time.

The encrypted seed phrase, along with other sensitive data like addresses, keys and account data, is securely saved in the browser’s local storage. No online app, website or provider can access any of that secured data - the user remains with total control over their wallet. To store and manage accounts, MetaMask’s [Eth-Keyring library](https://github.com/MetaMask/KeyringController) used. We leverage audited and proven open source solutions to minimize the possibility of error.

Along with keys and accounts, Tornado secrets need to be safely stored inside the browser extension’s storage. To keep a minimum surface of attack, all secrets needed for the zkSnarks are derived from the wallet’s seed phrase. This also means that the user only has to save the seed phrase to be able to import all wallet data, including the zkSnark secrets.

The following graphic shows how hierarchical deterministic (HD) wallets are integrated into Blank and how Tornado secrets can also be derived from the HD wallet structure.
