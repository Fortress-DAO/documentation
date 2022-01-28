# Dashboard

The dashboard shows relevant information about the project to its users. For now, our dashboard only shows a few graphs. We plan on adding many more in the near future.

![Dashboard page](<../.gitbook/assets/image (3).png>)

Let's explain these terms one by one, so you can fully understand what you're looking at.

### FORT Price

This is the price per one FORT on the open market. Currently, most of the liquidity is at TraderJoe. To watch the token's price, one can use [DexScreener](https://dexscreener.com/avalanche/0x3e5f198b46f3de52761b02d4ac8ef4ceceac22d6), [nomics](https://nomics.com/assets/fort3-fortress-dao), [CoinGecko](https://www.coingecko.com/en/coins/fortress-dao), or just [TraderJoe](https://traderjoexyz.com/#/trade?inputCurrency=0x130966628846BFd36ff31a822705796e8cb8C18D\&outputCurrency=0xf6d46849DB378AE01D93732585BEc2C4480D1fD5).

### wsFORT price

Calculated by multiplying FORT's price by the current index. This is because the conversion rate between wsFORT and sFORT is the same as the index.

### Market Cap

Market Cap represents the market value of all tokens together, calculated by multiplying the current price with the total amount of tokens.

### Supply (Staked/Total)

This value represents the amount of FORT tokens currently being staked on Fortress, in comparison to all existing tokens (even vested ones).

### TVL

Represents the dollar amount of all the staked FORT in Fortress.

### APY

Compounded interest earned by stakers in one year. It takes into account the effect of compounding since sFORT rebases exponentially.

### Current Index

Allows you to track your gain from staking. The index started from 1 at epoch 0, and increases every epoch. If you staked at genesis (epoch 0) and never unstaked any FORT, your balance today would be X times greater, where X is the current index. You can use the index to track your position by marking down the index number when you stake and unstake. You divide the index number when you unstake by the index number when you stake to get the ratio by which your sFORT balance has increased.

### Treasury Balance

Total dollar amount of tokens in Fortress's treasury.

### Backing per $FORT

Represents the dollar value of tokens backing FORT. The tokens backing FORT are safely stored in Fortress's treasury.

### Runway

Runway is the number of days that staking rewards can be distributed at current APY based on current risk-free value (RFV) in the treasury.
