# 2. Problems targeted

Unlike Bitcoin’s UTXO structure which offers greater privacy, Ethereum is built using an account-based model where a single address acts like a wallet and can make use of ETH or ERC-20 tokens without the need to transfer unspent balances. Although the practice of using a new address for each new transaction helps to reduce the data left behind, it’s impossible to hide all the information without relying on other services.

There are a few noteworthy problems on Ethereum:

## 2.1. Wealth Privacy

Holding wealth on centralised exchanges is never safe. Any literate investor would advise holding funds in a private wallet instead. By holding cryptocurrency in a private wallet, the user is still vulnerable to have himself or his wealth identified, if previous transactions were [analyzed](https://www.coindesk.com/coinbase-analytics-blockchain-analysis-crypto-government). Everyday transactions, such as sending payments to friends, become an excruciating task, as extreme effort is needed to preserve the privacy of wealth stored on chain. 

Amongst the safest approaches is grouping wealth with other individuals, making it impossible to distinguish capital ownership. Ethereum’s smart contracts enable the possibility of grouping wealth in a trustless manner. Blank’s approach to this can be found in section 3.2.

## 2.2. Origins Privacy

Ethereum’s ecosystem provides many financial opportunities: gambling, selling personal NFTs, speculating with controversial tokens and many more. After conducting these operations, in some instances, the user may not want to disclose how he accrued his wealth if it's irrelevant. 

Blank believes that unconnected parties shouldn’t know more about you than necessary. 

## 2.3. Trading Privacy (ETH, ERC-20)

On August 8th 2020, many prominent figures on Twitter [shared an address](https://twitter.com/HsakaTrades/status/1292175410550038529) identified as “Zeus Capital”, with an onchain short position on Chainlink. In the following hours, there were many follow up tweets inviting traders to “go long on $link and do a short squeeze”, which resulted in a $17M short liquidation for the identified trader. 

Despite the fact that the method used to identify the wallet is unclear, the use of multiple wallets and blurring the origins of funds could have made the identification a much more demanding task.

Similarly, on October 18th 2020, a known VC company PolyChain [has been identified](https://twitter.com/dcarmitage/status/1325942216108470272) as a large buyer of YFI tokens. Despite the fact that this identification has resulted in a positive outcome for Polychain, causing an influx of new buyers, we have yet to see a possible negative outcome of this identification - once the VC company decides to exit their positions, it’s likely markets would experience fear, uncertainty and doubt, provoking large negative price action.

Currently, there are no existing solutions that would allow to hide ERC-20 assets in a decentralized way, with more convenient methods to hide trading activity (that is, frictionlessly create new wallet for each new transfer and so on).


Blank aims to introduce ERC-20 pooling via smart contracts, allowing traders to become less visible. 
