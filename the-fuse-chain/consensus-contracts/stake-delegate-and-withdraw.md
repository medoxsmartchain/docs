---
description: 'Guides on how to stake, delegate and withdraw using myetherwallet.com'
---

# Stake, Delegate and Withdraw

The basic requirement to become a Nordek chain validator is to have a stake amount of at least 100,000 Nordek tokens. The stake amount is the sum of staked and delegated Nordek tokens of the address. This guide walks trough the process of using MEW \(MyEtherWallet.com\) in the process of using Nordek network.

{% hint style="warning" %}
**Roadmap** - Those functionalities will be built into our Studio and will not require any technical knowledge in the future.
{% endhint %}

## Stake

There are two options to stake \(both should be called from the address which would be the validator\)

1. Send Nordek tokens to the [consensus contract](https://nordekscan.com/address/0x3014ca10b91cb3d0ad85fef7a3cb95bcac9c0f79) - 0x8db1436097E3d16DD366c138F6953Fb7ee9a96Ad on the fuse network.
2. Call the \`stake\` function on the [consensus contract](https://nordekscan.com/address/0x3014ca10b91cb3d0ad85fef7a3cb95bcac9c0f79) - 0x8db1436097E3d16DD366c138F6953Fb7ee9a96Ad on the fuse network

 

## Delegate

Nordek token holders who don't want to run a node by themselves but still wish to participate in governing the network can delegate any amount to one of the validators.

Delegating is done by calling the \`delegate\` function on the [consensus contract](https://nordekscan.com/address/0x3014ca10b91cb3d0ad85fef7a3cb95bcac9c0f79) with the validator address as data \(see screenshot from MEW\).

![delegate](../../.gitbook/assets/screen-shot-2019-09-04-at-14.59.27.png)

## Withdraw

Both stakers and validators can withdraw their Nordek tokens, up to the staked/delegated amount, at any time. The withdrawn amount will be deducted from the validator stake amount, and if the stake amount becomes below the minimum stake amount - the validator will be removed from the Nordek chain validators list.

There are two options to withdraw:

1. Call the \`withdraw\` function on the [consensus contract](https://nordekscan.com/address/0x3014ca10b91cb3d0ad85fef7a3cb95bcac9c0f79) with one parameter - the amount to withdraw. This call is for stakers, and will reduce the stake amount of the sender address.
2. Call the \`withdraw\` function on the [consensus contract](https://nordekscan.com/address/0x3014ca10b91cb3d0ad85fef7a3cb95bcac9c0f79) with two parameters - validator address and amount to withdraw. This call is for both stakers \(who can use their own address as the parameter\) and for delegators to withdraw their delegated stake on a specific validator.

![withdraw option \#1](../../.gitbook/assets/screen-shot-2019-09-04-at-15.01.15.png)

![withdraw option \#2](../../.gitbook/assets/screen-shot-2019-09-04-at-15.01.25.png)

