# Blocktrail Wallet Recovery Tool
---------------------------------

This tool can be used to recover funds from a Blocktrail wallet using your backup file. It allows you to sweep all the funds from the wallet into any bitcoin address you provide.  

See the [live version of tool](http://blocktrail.github.io/wallet-recovery-tool/).

## Things to Know...
#####Supported Wallets
Both the developer API wallets and the consumer wallets (iOS, Android and web app) are supported by this tool.

#####Required Data
You need your backup pdf along with the password you used when you created the wallet. For the developer wallets, this is the password you give when you create each wallet. For the consumer wallets this is the password you used when signing up for an account.  
For users with a version 2 wallet (consumer wallet) you can recover you wallet even if you forget your password. This feature is only available if you signed up with your email address however. If you signed up with a username and have forgotten you password, please contact us directly at [support@blocktrail.com](mailto:support@blocktrail.com)

#####External Services Used
You can use the Blocktrail service to discover funds and send the transaction, or alternatively Bitpay Insight is also supported.

#####Finding your funds
When discovering funds, the tool will generate and check a batch of addresses. If funds are found in any of those addresses, another batch of addresses will then be generated and checked. This process continues until no funds are found in a batch of addresses.   
If you have a wallet which had a lot of activity, then it's possible that your funds are quite far down the chain of addresses. You will therefore need to specify a larger batch size. This will naturally take longer, but will ensure you discover all the funds in your wallet.

#####Importing your backup data
The tool can import and detect backup data directly from a backup pdf, however sometimes the QR Code detection encounters difficulties. You will need to scan the QR code with an external scanner in this case and input the pub key manually. [i-nigma](http://www.i-nigma.com/downloadi-nigmareader.html) has a free QR scanner for almost any mobile device. 
  
--------------------------------  
  
## Running This Tool Locally
The tool runs completely in your browser so your keys never leave your computer. It is possible to download this tool and run directly from your computer if you wish. 
You can either: 
1. Clone the repository, run `npm install` and then `gulp` to create you own build
2. Download the latest release which contains already built files 

Then you can use node and [serve](https://www.npmjs.com/package/serve) to create a local web server from the build folder. The tool will now be accessible locally through your browser.  
***NB:*** *the only steps that require an internet connection are the funds discovery (step 3) and relaying the signed transaction (final step)*
  
--------------------------------  
  
## Coming Soon...
- set the transaction fee manually
