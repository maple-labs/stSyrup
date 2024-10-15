# stSyrup

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)

This repo contains a set of contracts to facilitate on-chain distribution of protocol revenues denominated in Syrup tokens. Syrup distributions are made using RevenueDistributionToken (RDT) vesting schedule functionality. This allows for multiple deposits to be made to the same contract on a recurring basis with custom vesting parameters.

Please note stSyrup is a new contract re-deployed using the old xMPL Contract and can be found on [etherscan](https://etherscan.io/address/0xc7E8b36E0766D9B04c93De68A9D47dD11f260B45).

## Capabilities

stSyrup inherits the core functionality from Maple's [Revenue Distribution Token](https://github.com/maple-labs/revenue-distribution-token), which allows users to lock assets to earn rewards distributions based on a vesting schedule.

## Testing and Development
#### Setup
```sh
git clone git@github.com:maple-labs/stsyrup.git
cd stSyrup
forge update
```
#### Running Tests
- To run all unit/fuzz tests: `make test` (runs `./test.sh`)
- To run all invariant tests: `make invariant` (runs `./invariant.sh`)
- To run all tests (unit/fuzz and invariant tests): `make test-all`
- To run specific unit tests: `./test.sh -t <test_name>` (e.g., `./test.sh -t test_scheduleMigration`)
- To run specific invariant tests: `./invariant-test.sh -t <test_name>` (e.g., `./invariant-test.sh -t invariant_totalSupply`)
- To run specific fuzz tests with a specified number of fuzz runs: `./test.sh -r <runs>` (e.g., `./test.sh -t testFuzz_performMigration -r 10000`)

This project was built using [Foundry](https://github.com/gakonst/Foundry).

## Audit Reports
| Auditor | Report link |
|---|---|
| Trail of Bits | [ToB Report - April 12, 2022](https://docs.google.com/viewer?url=https://github.com/maple-labs/maple-core/files/8507237/Maple.Finance.-.Final.Report.-.Fixes.pdf) |
| Code 4rena | [C4 Report - April 20, 2022](https://code4rena.com/reports/2022-03-maple/) |

## Bug Bounty

For all information related to the ongoing bug bounty for these contracts run by [Immunefi](https://immunefi.com/), please visit this [site](https://immunefi.com/bounty/maple/). 

| Severity of Finding | Payout |
|---|---|
| Critical | $50,000 |
| High | $25,000 |
| Medium | $1,000 |

## About Maple
[Maple Finance](https://maple.finance) is a decentralized corporate credit market. Maple provides capital to institutional borrowers through globally accessible fixed-income yield opportunities.

For all technical documentation related to the currently deployed Maple protocol, please refer to the maple-core GitHub [wiki](https://github.com/maple-labs/maple-core/wiki).

---

<p align="center">
  <img src="https://user-images.githubusercontent.com/44272939/116272804-33e78d00-a74f-11eb-97ab-77b7e13dc663.png" height="100" />
</p>
