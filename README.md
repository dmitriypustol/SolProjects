# ERC20 Staking Contract
ERC20 Staking Contract
Overview
This Solidity smart contract implements a secure staking mechanism where users can stake one ERC20 token to earn rewards in another ERC20 token. The contract features:

Customizable APY (Annual Percentage Yield)

Adjustable lock periods

Emergency withdrawal functionality

Reward accumulation calculations

Owner-controlled parameters

Key Features
For Users
Stake Tokens: Deposit supported ERC20 tokens to start earning rewards

Withdraw: Retrieve staked tokens after the lock period expires

Claim Rewards: Collect accumulated rewards at any time

Emergency Withdraw: Retrieve staked tokens (without rewards) during contract emergencies

For Contract Owner
Adjust APY: Set the annual percentage yield (max 100%)

Set Lock Period: Configure the staking duration (max 1 year)

Emergency Stop: Pause normal operations in case of issues

Withdraw Rewards: Recover reward tokens from the contract

Technical Details
Solidity Version: 0.8.0

Dependencies: OpenZeppelin's SafeERC20 and Ownable contracts

Security: Includes emergency stop pattern and safe transfer operations

Events: Comprehensive event logging for all key operations

Usage
Deploy the contract with staking token, reward token, and initial APY

Users call stake() to deposit tokens

After lock period, users can withdraw() their staked tokens

Users can claimRewards() at any time

Owner can adjust parameters as needed

Safety Features
Reentrancy protection through OpenZeppelin's SafeERC20

Input validation for all user-provided data

Emergency withdrawal mechanism

Proper access control for admin functions

This contract is suitable for projects looking to implement a secure, customizable staking mechanism with ERC20 tokens.
