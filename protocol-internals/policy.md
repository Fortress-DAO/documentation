# Policy

Fortress features policy constants that allow us to optimise the system.

## Minting

The **BCV** allows us to scale the rate at which bond premiums increase. A higher BCV means a lower discount for minters and more protocol profit. A lower BCV means a higher discount for minters and less protocol profit. We can also include a minimal price for which one FORT is sold.

The **vesting term** determines how long it takes for bonds to become fully redeemable. A longer term means lower inflation and lower bond demand.

## Sales

The **DCV** allows us to scale protocol buy pressure up or down. A higher DCV means more buy pressure and higher deflation. A lower DCV means less buy pressure and a weaker floor.

## Treasury

Profit Allocations are the only treasury variable. This allows us to choose who receives profits from the protocol.

## Staking

There are no variables in the staking contract. FORT and sFORT are always redeemable 1:1, and profits are always distributed equally through rebase.
