---
layout: post
title: "light.wallet"
---

![light-wallet](/images/light-wallet/light-wallet.png)

_**A hardware wallet for the next billion**_

### Introduction

The idea of a hardware wallet is nothing new. There are already lots of companies operating in this domain, with [Ledger](https://www.ledger.com/) and [Trezor](https://trezor.io/) being the most well-known. However, if one takes a closer look at the products currently on the market it becomes clear that there isn't really anything that could scale to the next billion of users. This comes down to the following three factors: expensive, not user-friendly and not durable. The light.wallet offers a solution to all three problems, enabling the entrance of the next billion into safely storing and using Bitcoin. 

### Next billion

Hypothesis: Bitcoin will become the preferred currency of choice in developing countries _before_ the developed ones. Why? Our argument is that this mainly comes down to 2 factors:

1. High inflation: many developing countries suffer from high rates of inflation, investing in Bitcoin can be a hedge against this kind of instability and a reliable way to build wealth.
2. 1.7 billion unbanked ([worldbank.org](https://globalfindex.worldbank.org/sites/globalfindex/files/chapters/2017%20Findex%20full%20report_chapter2.pdf)): "Globally, about 1.7 billion adults remain unbanked-without an account at a financial institution or through a mobile money provider."

The latest data seems to support this hypothesis. For example, the [2021 Geography of Cryptocurrency Report](https://go.chainalysis.com/rs/503-FAP-074/images/Geography-of-Cryptocurrency-2021.pdf) shows that the countries with the highest amount of P2P exchange volume (adjusted for PPP per capita) are:

1. Kenya
2. Togo
3. Vietnam
4. Tanzania
5. Cameroon

### What's the problem?

Most users of crypto in the developing world use their (smart)phone as a wallet. However this has some significant downsides:

1. Loss/theft: given the fact that a phone is something carried daily, it is at a significant risk of being lost or stolen. Especially when this becomes your de-facto savings account this becomes an extremely high risk, an unfortunate accident/situation could mean losing all your funds.
2. Battery life: as smartphones are often prone to running out of battery, this means that you're always dependent on having a charge whenever you want to make a transaction. This can be incredibly inconvenient.

The solution is to use a hardware wallet. However, if we take a look at the currently available models, we'll see that they all carry significant downsides:

_Ledger Nano S_

```
- Requires a computer/usb-cable connection to use
- Not very durable/waterproof
- Making a transaction is cumbersome
- Expensive (€60)
```

_Trezor T_

```
- Requires a computer/usb-cable connection to use
- Not very durable/waterproof
- Making a transaction is cumbersome
- Expensive (€65)
```

_Ledger Nano X_

```
+ Wireless (Bluetooth)
- Not very durable/waterproof
- (Prohibitively) expensive (€120)
```

_Coldcard_

```
+ Does not require a computer (air-gap)
- Not very durable/waterproof
- (Prohibitively) expensive ($130)
```

### What's the solution?

The solution to this problem needs to check the following criteria/constraints:

1. Secure: a secure wallet means that your funds can be stored safely, even if someone steals your wallet, they should not be able to access your funds.
2. Durable: if it is to be adopted by a large number of people, living in a wide range of climates, it is clear that durability is an important feature.
3. Affordable: makes it accessible to the widest range of people, regardless of their financial situation.
4. Easy-to-use: should not require any special knowledge/skills to use.
5. KaiOS/Android: assume that the only internet-connected device available is a very basic phone. [KaiOS](https://en.wikipedia.org/wiki/KaiOS) is a popular OS for (cheap) feature phones that nevertheless offer internet connectivity (and a small app store).

This is how the light.wallet will look like:

![wallet-front-back](/images/light-wallet/wallet-front-back.png)

Now, let's go through the criteria one-by-one again:

#### Secure

The security is based on a minimal attack surface principle. A common type of hack is called "[side-channel attack](https://en.wikipedia.org/wiki/Side-channel_attack)" and is based on extracting information from the device through analysing power usage or detecting EM waves. By not providing any access to the battery (which can be charged by the solar cell), we can already effectively eliminate the possibility to analyse the power usage. By adding a metallic foil on the inside of the casing of the wallet, we also eliminate the possibility of extracting (or affecting) the data of the device through the use of EM waves. Finally, the device should be constructed in such a way that it can't be disassembled without destroying the circuitry containing the private keys. All this should contribute to a wallet, which while simple in its approach, still offers plenty of security. As there is no need for any special secure electronic components, this approach also offers a high degree of security at the lowest price.

#### Durable

There are no ports on the device, the keyboard is integrated in the casing as well, much in the same way as done on the 2FA-authentication device shown below. Waterproofing such a device should not be a great challenge and can be done quite cheaply. 

![2fa-device](/images/light-wallet/2fa-device.png)

#### Affordable

Our estimate is that a large part of the cost of other wallets comes from using special, expensive components such as secure elements or bluetooth chips. As our approach to security does not require any secure elements and the communication is mainly done through the keyboard and led/light-sensor, it should come at a significantly lower price-point that the competition.

#### Easy-to-use

The keyboard offers an easy and universally understood interface (something which can't be said for some other wallets). When transmission of data is required, this is done through VLC ([Visible Light Communication](https://en.wikipedia.org/wiki/Visible_light_communication)) using the LED, giving a visual confirmation of the transaction to the user.

#### KaiOS/Android

Assuming the most basic of phones with an internet connection, this wallet can still be used. The only requirement for making a transaction is a flash-light and a camera-module, which can be found on even the cheapest models (some of which don't have Bluetooth).

We have already mentioned VLC, but what do we mean exactly?

For making a transaction, a signing has to occur on the wallet and that signature (data) needs to be transmitted to the internet. Currently available wallets do this in one of 2 ways: USB or Bluetooth. Both have some significant downsides. USB requires an additional cable and a port which can be a liability when it comes to durability. Bluetooth is more expensive and uses additional power, leading to a reduced battery life. 

Our solution is to integrate a LED and light-sensor on the back of the wallet, which can be used to communicate (in both directions) with the phone (which is in turn connected to the internet). A 'basic' bitcoin transaction requires ~250 bytes of data (2000 bits). Assuming that the phone camera has a refresh rate of 15 Hz, this means a transaction can be transmitted in ~2 minutes. Given the rate of improvement of smartphone cameras and the subsequent drop in cost, it is safe to assume that even the most basic phones will soon have 60 Hz cameras, which would result in a transmission time of ~35 seconds. As phone usage has wide penetration, even in the most remote parts of the world, this could mean a true revolution in terms of making payments.

![vlc-communication](/images/light-wallet/vlc-communication.png)

#### Battery life

And last but not least, let's talk about battery life. Since there is no external way to charge the device, integration of a solar cell solves this by allowing it to easily be recharged by sunlight. Solar cells are, much in the same way as smartphone cameras, continually improving and getting cheaper and therefore should not cause a great increase in the final unit cost. On the power consumption side, we can also mention that by using VLC it should be possible to greatly reduce the required power in comparison to other wireless solutions such as Bluetooth. In the end, the product life of this wallet will be measured in years (or even decades). 

### Conclusion

The light.wallet offers a completely new approach to hardware wallets, with the potential to play a crucial role in the further adoption of Bitcoin around the world. Our hope is that it can become the Nokia 3310 of hardware wallets and just as ubiquitous. We believe that by empowering everyone to become their own bank, the world will become more prosperous and fair. 

[Part 2](https://maksimdrachov.github.io/2022/09/01/light-terminal)