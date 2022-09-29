ERC-20 Token SWAPPING_CONTRACT




What is Swapping ?
Swap is a token-to-token exchange. Swap allows users to easily exchange one token with another without leaving their explorer. 

Ethereum Token Swapping :

You can Swap your Tokens with another without going through several intermediaries, which will also cost gas fees. You can swap your TokenA with TokenB.

Uniswap Exchange :

Use a Solidity smart contract to swap tokens on Uniswap. Uniswap is a decentralized exchange running on the Ethereum blockchain. It is a set of Solidity smart contracts that work together to create an automated market maker environment that requires no human intervention. Automated market maker exchanges allow digital assets to be traded automatically without permission. They use liquidity pools instead of a traditional order book of buyers and sellers.




Implementation:-
SwappingExchange:https://goerli.etherscan.io/address/0x4451ba4afe6f7534b5817ca1fb9fe092c8a0b12d#code



ERC20 Swapping :

Now, we are going to focus on creating a Swapping contract (ERC20 Based). As you know the ERC20 Token is open zeppelin Standard. We are just using the Interface of deployed Staking Token () and Reflectionary/Reward Token as ER20-based Token.


NOTE:- We are using Interface in this Contract. You can learn about the Smart Contract Interface by providing the link (https://www.newline.co/courses/creating-an-erc20-token-on-ethereum/smart-contract-interfaces)


Now, we see the Read and Write functions of Swapping on Remix Ide after compiling and deploying. And also can check on EtherScan Goerli Testnet given link (https://goerli.etherscan.io/address/0x4451ba4afe6f7534b5817ca1fb9fe092c8a0b12d#code) of deployed contract.

Read Functions:-

1. coin: This function returns the contract address of the coin.

2. coinPrice: This function returns the price of a coin.

3. soldCoins: This function returns the sold coins.

4. exchangeLiquidity: This function returns the value(uint type) of tokens and coins liquidity in contract.

5. getFees: This function returns the percentage of fee (uint type) of exchange.

6. getRatio : This function returns the percentage of ratio exchange.

7. token : This function returns the token address.

8. tokenPrice : This function returns the price(uint type in wei) of a token.

9. soldTokens : This function returns sold tokens.

Write Functions:-
1. buyCoins : You can buy coins according to price and inputting number of coins. 

2. buyTokens : You can buy tokens according to price and inputting number of tokens. 

3. changeCoinPrice : This function will set a new price of a coin. 

4. changePrice : This function will set a new price of a token . 

 5. setFees : This function will set the percentage fee of exchange. 

 6. setRatio :This function will set the percentage  ratio of exchange. 

 7. swapCoinToToken : You can Swap Coin to Token  with this function. First, approve this contract the amount you want to swap. 

 8. swapTokenToCoin : You can Swap Token  to Coin with this function. First, approve this contract the amount you want to swap. 



Deployment Procedure:-

Step 1: First of all you have deployed a Token Contract Address. If not then first deploy the Token you want to use.Then you need a code of Token(erc20 based) for  deployment.If you have code of Token, then well and good,otherwise you can use  ERC20_TokenA ,using this link, you will go to the EtherScan Explorer,just copy the code from the explorer contract address and paste it in the Remix as your token name and file.
In our case we have a deployed contract address of token (ER20_TokenA). You can use it.

Step 2: Then after step 1 you have also deployed another Token/Coin Contract Address for swapping. If not then also deploy the other Token/Coin you want to use.Here you can repeat step 1 procedure, just for another token/coin address,also you can use it ERC20_TokenB. 
In our case we have a deployed contract address of token (ER20_TokenB). You can use it.
Step 3: Then after both step 1 and step 2 . Final step of deployment procedure. In this step we will use the Swapping Exchange contract for the deployment.
When we are gone to deploy the Swapping Exchange Contract it needs the Address of Token and Token/Coin. That is already done above step 1 and step 2. Just put addresses of token and Token/Coin and also token and coin price.
After given the above inputs deploy the contract.

Here is a video link for Deployment of Contract Using Remix Ide. Ethereum Smart Contract with Remix






Usage Flow:-

After deploying all three contracts e.g: Swapping Exchange , ERC20_TokenA & ERC20_TokenB .

Step 1: Transfer totalSupply (or how much total Swap_Supply you want to give) of TokenA & TokenB ( Make sure you give an equal amount of SwapSupply to the contract) to the tokenSwap contract.

Step 2: Approve the amount you want to swap from the Token contract (if swapping Token to Coin). Then swap that amount through the SwappingExchange contract.

Step 2: Approve the amount you want to swap from the Coin contract (if swapping Coin to Token). Then swap that amount through the Swapping Exchange contract.

Changes:- 

You can change the fee  value (uint type). Now it is 1, which means 1 %.
You can change the ratio value (uint type). Now it is 1, which means 1%.
 





Disclaimer:-

This ERC-20-based Swapping smart contract was created for use in production-level blockchain applications and is thoroughly tested to the best of the developers' knowledge to work as intended.



That's it! you're done. 