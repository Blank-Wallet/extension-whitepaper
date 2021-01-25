# 1.1. Overview

In 2020 we had a chance to experience a true paradigm shift. In line with the ever-increasing demand for privacy and anonymity, a new subset of the crypto ecosystem emerged. While the theoretical concept of avoiding centralised parties has been around since the inception of Bitcoin, the Decentralised Finance (DeFi) market bloom in 2020 demonstrated the true potential of putting such ambitious ideas into action. 

Not to mention, DeFi structures have been constructed on strong, value-driven foundations: decentralization, immutability, and absence of central, infinitely powerful bodies. The wider user base seems to agree with these calls for change - and the numbers show it. According to DeFi Pulse, the Total Value Locked (USD) in DeFi has been hitting all-time highs almost daily since the Q2 of 2020.

With that, timely and well-executed DeFi platforms proved to be a force to be reckoned with. For example, Uniswap, providing a decentralized Ethereum based protocol that allows users to safely exchange ERC-20 tokens, has reached $3 billion in total value locked. Launched just 2 years ago and growing at a neck-breaking rate, Uniswap has already surpassed 250,000 unique addresses and supported over $20B worth of trades. Several DeFi lending platforms - MakerDAO, Compound, Aave - enjoyed comparable success, having each locked north of $1B to date. 

**The need for a solution** <br/> When one thinks about the values and beliefs behind blockchain technology, it’s evident that transparency and immutability go hand in hand for all dominant blockchains.

Immutability, the original value proposition of blockchain technology, is still the leading benefit sought after by the public, when participating in any DeFi activities.

Transparency, on the contrary, is not as cherished: if given the option, consumers choose to remain anonymous over revealing themselves and their wealth. 

Observing the issues in the DeFi space, a demand for anonymity is clear: BitMEX website visits in 2020 indicate a clear correlation between the desire to remain anonymous when proceeding with trading activities: after the Aug 14th 2020 announcement of mandatory KYC, website visits dropped 35% from 5.3 million visits in August 2020 to 3.4 million visits in October 2020, and hasn’t reached highs ever since. 

With today’s existing solutions, users must either experience friction or deal with centralised entities if they wish to remain less transparent and anonymous when participating in DeFi ventures.

**Blank wallet fights both friction and centralisation.** <br/>  Blank believes everyone should have rights to their privacy. Privacy shouldn’t be “opt-in”, rather it’s something you could occasionally “opt-out” on your free will.

## 1.2. What is Blank?

Blank is the most private, non-custodial Ethereum browser wallet.

Blank uses smart contracts that allow users to hide the amounts and origins of cryptocurrency held, in a decentralized and frictionless manner. 

Each time you want to make a withdrawal, Blank will create a new wallet address for you with the amount of crypto that you requested, which originates from the smart contract where everyone’s funds are pooled.

## 1.3. Blank Wallet Preview

Below is a preview of how the Blank wallet looks. While some of the buttons on this mockup bring you to new screens, this is just a showcase with very limited functionality.

<style>
    .lds-dual-ring {
        display: inline-block;
        width: 80px;
        height: 80px;
        position: absolute;
        left: calc(50% - 48px);
        top: calc(50% - 48px);
    }
    .lds-dual-ring:after {
        content: " ";
        display: block;
        width: 64px;
        height: 64px;
        margin: 8px;
        border-radius: 50%;
        border: 6px solid black;
        border-color: black transparent black transparent;
        animation: lds-dual-ring 1.2s linear infinite;
    }
    @keyframes lds-dual-ring {
        0% {
            transform: rotate(0deg);
        }
        100% {
            transform: rotate(360deg);
        }
    }
</style>
<div style="position: relative; width: 360px; max-width: 100%; height: fit-content;">
    <div style="position: relative; display: flex; align-items: center; justify-content: center; height: 0; padding-top: calc(600 / 360 * 100%); border: 1px solid rgba(0, 0, 0, 0.1); border-radius: 0.75rem; overflow: hidden;">
        <div class="lds-dual-ring" style="opacity: 0.1;"></div>
        <iframe style="position: absolute; left: 0; top: 0; width: 100%; height: 100%; border: none;" width="100%" height="100%" src="https://www.figma.com/embed?embed_host=share&url=https%3A%2F%2Fwww.figma.com%2Fproto%2FVuKEhYNbfxfE4h5dXa6Cu4%2FWallet-Preview%3Fnode-id%3D1%253A257%26scaling%3Dmin-zoom%26hide-ui%3D1" allowfullscreen></iframe>
    </div>
</div>