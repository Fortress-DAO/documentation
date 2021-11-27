# Equations

## Staking

$$
deposit = withdrawal
$$

Swaps between FORT and sFORT during staking and unstaking are always honored 1:1. The amount of FORT deposited into the staking contract will always result in the same amount of sFORT. And the amount of sFORT withdrawn from the staking contract will always result in the same amount of FORT.

$$
rebase = 1 - ( fortDeposits / sFORTOutstanding )
$$

The treasury deposits FORT into the distributor. The distributor then deposits FORT into the staking contract, creating an imbalance between FORT and sFORT. sFORT is rebased to correct this imbalance between FORT deposited and sFORT outstanding. The rebase brings sFORT outstanding back up to parity so that 1 sFORT equals 1 staked FORT.

## Minting

$$
mint Price = 1 + Premium
$$

FORT has an intrinsic value of 1 MIM, which is roughly equivalent to $1. In order to make a profit from minting, Fortress charges a premium for each bond.

$$
Premium = debt Ratio * BCV
$$

The premium is derived from the debt ratio of the system and a scaling variable called [BCV](https://docs.olympusdao.finance/references/glossary#bcv). BCV allows us to control the rate at which mint prices increase.

The premium determines profit due to the protocol and in turn, stakers. This is because new FORT is minted from the profit and subsequently distributed among all stakers.

$$
debt Ratio = mintsOutstanding/fortSupply
$$

The debt ratio is the total of all FORT promised to minters divided by the total supply of FORT. This allows us to measure the debt of the system.

$$
mintPayout_{reserveBond} = marketValue_{asset}\ /\ mintPrice
$$

Mint payout determines the number of FORT sold to a minter. For reserve bonds, the market value of the assets supplied by the minter is used to determine the bond payout. For example, if a user supplies 1000 MIM and the mint price is 250 MIM, the user will be entitled 4 FORT.

$$
mintPayout_{lpBond} = marketValue_{lpToken}\ /\ mintPrice
$$

For liquidity bonds, the market value of the LP tokens supplied by the minter is used to determine the bond payout. For example, if a user supplies 0.001 FORT-MIM LP token which is valued at 1000 MIM at the time of bonding, and the mint price is 250 MIM, the user will be entitled 4 FORT.

## FORT Supply



$$
FORT_{supplyGrowth} = FORT_{stakers} + FORT_{minters} + FORT_{DAO} + FORT_{vestedTeamTokens}
$$

FORT supply does not have a hard cap. Its supply increases when:

* FORT is minted and distributed to the stakers.
* FORT is minted for the minter. This happens whenever someone mints FORT.
* FORT is minted for the DAO. This happens whenever someone mints FORT. The DAO gets the same number of FORT as the minter.

$$
FORT_{stakers} = FORT_{totalSupply} * rewardRate
$$

At the end of each epoch, the treasury mints FORT at a set reward rate. These FORT will be distributed to all the stakers in the protocol.&#x20;

$$
FORT_{minters} = mintPayout
$$

Whenever someone mints FORT, a set number of FORT is minted. These FORT will not be released to the minter all at once - they are vested to the minter linearly over time. The mint payout uses a different formula for different types of bonds.&#x20;

$$
FORT_{DAO} = FORT_{minters}
$$

The DAO receives the same amount of FORT as the minter. This represents the DAO profit.

## Backing per FORT

$$
FORT_{backing} = treasuryBalance_{stablecoin} + treasuryBalance_{otherAssets}
$$

Every FORT in circulation is backed by the Fortress treasury. The assets in the treasury can be divided into two categories: stablecoin and non-stablecoin.

$$
treasuryBalance_{stablecoin} = RFV_{reserveBond} + RFV_{lpBond}
$$

The stablecoin balance in the treasury grows when bonds are sold. RFV is calculated differently for different bond types.

$$
RFV_{reserveBond} = assetSupplied
$$

For reserve bonds such as the MIM bond, the RFV simply equals to the amount of the underlying asset supplied by the minter.

$$
RFV_{lpBond} = 2sqrt(constantProduct) * (\%\ ownership\ of\ the\ pool)
$$

For LP bonds such as FORT-MIM bond, the RFV is calculated differently because the protocol needs to mark down its value. Why? The LP token pair consists of FORT, and each FORT in circulation will be backed by these LP tokens - there is a cyclical dependency. To safely guarantee all circulating FORT are backed, the protocol marks down the value of these LP tokens, hence the name _risk-free_ value (RFV).
