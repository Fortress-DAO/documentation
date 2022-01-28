# Dashboard

The dashboard shows relevant information about the project to its users using text and graphs. Each one has an information bubble next to it. When you hover your mouse over it, an explanation of the term will show up.

![](<../.gitbook/assets/Screenshot 2022-01-28 at 19.42.15.png>)

As to make this simpler to read all at once and you can fully understand what you're looking at., let's explain these terms one by one.

### FORT Price / wsFORT price

FORT: This is the price per one FORT on the open market. Currently, most of the liquidity is at TraderJoe. To watch the token's price, one can use [DexScreener](https://dexscreener.com/avalanche/0x3e5f198b46f3de52761b02d4ac8ef4ceceac22d6), [nomics](https://nomics.com/assets/fort3-fortress-dao), [CoinGecko](https://www.coingecko.com/en/coins/fortress-dao), or just [TraderJoe](https://traderjoexyz.com/#/trade?inputCurrency=0x130966628846BFd36ff31a822705796e8cb8C18D\&outputCurrency=0xf6d46849DB378AE01D93732585BEc2C4480D1fD5).

wsFORT: Calculated by multiplying FORT's price by the current index. This is because the conversion rate between wsFORT and sFORT is the same as the index.

### Supply (Staked/Total)

This value represents the amount of FORT tokens currently being staked on Fortress, in comparison to all existing tokens (even vested ones).

### APY

Compounded interest earned by stakers in one year. It takes into account the effect of compounding since sFORT rebases exponentially.

### Current Index

Allows you to track your gain from staking. The index started from 1 at epoch 0, and increases every epoch. If you staked at genesis (epoch 0) and never unstaked any FORT, your balance today would be X times greater, where X is the current index. You can use the index to track your position by marking down the index number when you stake and unstake. You divide the index number when you unstake by the index number when you stake to get the ratio by which your sFORT balance has increased.

### Backing per $FORT

Represents the dollar value of tokens backing FORT. The tokens backing FORT are safely stored in Fortress's treasury.

### Runway

Runway is the number of days that staking rewards can be distributed at current APY based on current risk-free value (RFV) in the treasury.

### Total Value Deposited

Represents the dollar amount of all the staked FORT in Fortress.

### Market value of Treasury Assets

Total dollar amount of non-native tokens (everything but FORT) in Fortress's treasury.

### Risk Free Value of Treasury Assets

Total dollar amount of stablecoins in treasury.

### Protocol Owned Liquidity (POL) <a href="#pol" id="pol"></a>

Protocol Owned Liquidity, is the amount of LP the treasury owns and controls. The more POL the better for the protocol and its users.

### FORT Staked (%)

Tracks the amount of circulating FORT tokens in % being staked on Fortress.

### Market Cap

Market Cap represents the market value of all tokens together, calculated by multiplying the current price with the total amount of tokens.

