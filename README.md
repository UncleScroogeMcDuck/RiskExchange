# RiskExchange Lightpaper

Name: RiskExchange Protocol

SmartContract: EVM Solidity

Version: 0.9

## Problem

1. Provide decentralized insurance to crypto users, including coverage of DeFi and others
2. Let the market define the price of risk instead of a centralized actuary

## Innovation

There are several interesting experiments in this area, such as Nexus Mutual and Cover Protocol.
The innovations of RiskExchange Protocol are:

1. It is perpetual cover
2. It covers multiple DeFi products in once
3. It use re-balance method which simplified the  process and reduce gas cost
4. Its pay as you go for coverage seekers

## Overview

![riskexchange3](http://qiniu.eth.fm/2021-07-15-riskexchange3.png)


## Roles

1. Liquidity Providers - seek for LP reward and swap fee
2. Coverage Seekers - seek for insurance
3. Prediction Market Users - take risk and seek for arbitrage

## How it works

### 1 Liquidity Providers

Deposit 1 DAI to the protocol, and mint 1 SAFU token and 1 RISK token

Create SAFU-DAI and RISK-DAI LP in Balancer, and get balancer fee and REX token reward

### 2 Coverage Seekers

Buy SAFU from Balancer

1 SAFU can claim 1 DAI when risk happens

When they do not need coverage any more, Coverage Seeker can sell SAFU any time on Balancer, or they can buy same number of RISK token send back to the contract and get DAI

### 3 Prediction Market Users

Buy RISK from Balancer when they think the RISK token price (risk) is under estimate

They can quit any time through sell RISK on Balancer, or they can buy same number of SAFU token send back to the contract and get DAI

### 4 Claim

When risk happens, SAFU holder can submit claim request, which will go through the RiskExchange governance process.

If the claim request got approved, requestor's SAFU token will be burned, and requestor will get the same number of DAI from the contract. At the same time, same number of RISK token will be burned and rebalance will be executed for all RISK token holders.
1% of claimed DAI will be processed as fee and will goes to the treasury.

## Governance

Governance is more focused on 3 areas:
1. Protocol upgrade
2. Coverage changes
3. Claim requests

There will be 2 level of governance. Council team will be elected first to filter the requests for the first round.

2nd level referendum will be processed on snapshot by all REX holders.

## Other Considerations

### Prevent adverse selection

1. There will be 30 days probation period for all SAFU holders, which means he need to hold SAFU tokens for more than 30 days if not, the claim process will be rejected.
2. Claim date is limited, requestor cannot claim for risks 1 month ago
3. Pledge is needed for all claims

### More Scenario

RiskExchange is an open platform which can be used for DeFi coverage and also healthcare coverage as well in the future.

## Feedback

https://github.com/UncleScroogeMcDuck/RiskExchange/issues



