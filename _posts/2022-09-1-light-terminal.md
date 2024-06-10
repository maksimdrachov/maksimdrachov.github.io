---
layout: post
title: "light.terminal"
---

![images/light-terminal/light-terminal-header.png](/images/light-terminal/light-terminal-header.png)
_**A payment terminal for light.pay**_

### Introduction

Previously we have introduced the idea for the [light.wallet](https://maksimdrachov.github.io/2022/08/31/light-wallet), a hardware wallet that uses a light-based protocol for transmitting information back-and-forth (called **light.pay**).

When using the wallet in combination with a phone, each transaction takes somewhere between 1 to 3 minutes. As the primary use case of the wallet is to store value, it is safe to assume such withdrawals won't need to be made very often. Indeed it might even be seen as a benefit: it introduces some friction whenever you want to withdraw, thereby encouraging you to hodl.

However, as the adoption and usage of Bitcoin grows, increasingly it'll be used as a regular currency as well (paying for groceries, taxi, coffee,...). To make these kind of daily transactions as quick and easy as possible, we want to introduce a new project: **light.terminal**. 

### How does it work?

Let's start by taking a look at how a transaction is signed using the light.wallet:

![lightpay-steps](/images/light-terminal/lightpay-steps-2.png)

Steps 1 and 3 use light.pay to transmit information back-and-forth. Assuming we use the phone's camera (30 Hz) and screen (60 Hz); a transaction takes roughly 3 minutes. To optimize the user experience for daily transactions, we need a way to increase the speed of transmitting information between the wallet and the phone by multiple orders of magnitude. 

![light-terminal](/images/light-terminal/light-terminal.png)

This is where the light.terminal comes into play, it's a square-shaped box that connects to the merchant's phone. It integrates a light-sensor and LED (same setup as the light.wallet) and 2 magnets that allow for easy allignment between the sensors/leds of the terminal and the customer's wallet. This circumvents the bottleneck in transmission speed, reducing the time it takes to make a payment down to a fraction of a second. This is done without requiring any special hardware (nfc, bluetooth, batteries) and works even with the most basic feature phone (which are popular in developing countries where we could envision this being used by cab drivers, street merchants,...)

To give credit where credit is due: we were (heavily) inspired by the [Square card reader](https://squareup.com/us/en/hardware/reader), which uses the same concept but applied to credit cards. 

![square-card-reader](/images/light-terminal/square-card-reader.png)

### Conclusion

The light.terminal allows for anyone to quickly setup a payment terminal that is as easy to use as the credit card, without needing to go through a centralized authority such as a bank or cryptocurrency exchange. This further decreases the barrier for anyone to start earning and doing business in Bitcoin. 