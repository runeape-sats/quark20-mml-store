# quark20-mml-store
**In digital worlds, creators and artists shall be free from governance.** 

[Spirit0](https://x.com/SPIRIT_0_247) came to [me](https://x.com/runeape_sats) saying that artists should have their own stores showcasing and selling their arts _permissionless_. This motivated me to build a 3D store infrastructure based on [MML](https://mml.io/) (describing spatial attributes of 3D objects), [BlocksOfBitcoin](https://x.com/BlocksOfBitcoin) (building 3D worlds on BTC blocks), and [Nakamoto Matrix](https://x.com/NakamotoMatrix) (crosschain interoperable digital world playground on web/unreal engine). Join our [Discord](https://discord.gg/Y7AwD7tpS9) to see what's happening.

Here are our showcase 3D store webpages:

- [chapy.blocksofbitcoin.xyz](http://chapy.blocksofbitcoin.xyz) (accepting BTC payments from Xverse)
- [spirit0.blocksofbitcoin.xyz](http://spirit0.blocksofbitcoin.xyz) ((accepting BTC payments from Xverse)
- [runeape.blocksofbitcoin.xyz](http://runeape.blocksofbitcoin.xyz) (accepting BTC payments from Xverse and $qAI SOL tips from Phantom. Both works in Xverse or Phantom mobile app)

![image](https://github.com/user-attachments/assets/b4e89bd9-11fb-4adb-b80e-363b9d4fcbeb)


## Quick Start

You can build and publish your 3D store page using ARC and MML. Note that MML is interoperable with other MML-based 3D world such as Yuga Labs OtherSide or any Improbable/M-Squared projects.

1. [free] go to ARC https://arc.blocksofbitcoin.xyz/ using desktop Chrome browser and check out the automated MML tutorial through experiential learning. You need basic idea of 3D coordinates and how to place 3D objects in desired locations with correct modifications of rotation and scale. Check out related XML and MML resources. 
2. To save your MML works, you need to sign-in with your Xverse wallet that owns [Nakamoto Matrix](https://magiceden.us/ordinals/marketplace/nakamotomatrix) (total supply: 798) for at least one day. For [$qAI](https://dexscreener.com/solana/9nhezuhqvat7vhktdwteguh9xryndeqhmvyvjfr7kpsz) holders, they can sign-in with Phantom
3. To debug MML, use [XML formatter](https://jsonformatter.org/xml-validator) for checking basic syntax errors (or ask AI?)
4. To publish your MML works into a 3D store with a designated web page, you need to enclose your MML document as `<m-store> ...your MML... </m-store>` where `<m-store>` is at the beginning and ending with `</m-store>` 


## m-store

This is a new tag we defined that currently only works in Quark20 ecosystem. `m-store` tags need to enclose your whole MML document `<m-store>...your mml...</m-store>`.

Follow the instructions to configure and customize your store:
- `title` (required): your store name
- `shortDescription` (required): short description
- `endUnixTimeStamp` (required for preorder or whitelisting): store sales ending timestamp. find a timestamp (in the future) here https://www.unixtimestamp.com/ when the store button disappeared, check if this timestamp expired.
- `depositBTCAddress` (required for preorder or whitelisting): for receiving BTC deposit to your BTC payment address
- `preOrderItem` (required for preorder): item name such as "Member Pass"
- `priceSats` (required for preorder): price in sats such as "10000"
- `whitelistItem` (required for whitelisting): item name such as "VIP Pass"
- `whitelistSats` (required for whitelisting): price in sats such as "10000"
- `storeLogo`: an image url to be placed as logo
- `depositQaiAddress` (required for accepting qAI as tips): your SOL address
- `tippingQai`: custom tip qAI amount such as "10000" (~$2)

Example store setup with pre-order button for "Member Pass" and a $qAI tip button:
```
<m-store
  title="My Nakamoto Store"
  shortDescription="The Cool Store in Nakamoto Matrix"
  endUnixTimeStamp="1753945200"
  preOrderItem="Member Pass"
  priceSats="10000"
  depositBTCAddress="35UR68XPKRHLDW4nXheGVEYAfSPzBvnVvV"
  tippingQai="10000"
  depositQaiAddress="4TJKs8R55JZEqEe7hFYVJYpQE6CJwGsXAQhSYvF5mS5E"
> <!-- your mml -->
</m-store>
```

Another store example:
```
<m-store
  title="Nakamoto Temple"
  shortDescription="The Only Temple in Nakamoto Matrix"
  endUnixTimeStamp="1753945200"
  whitelistSats="10000"
  whitelistItem="VIP Pass"
  storeLogo="https://quark20a.s3.us-west-1.amazonaws.com/q/sq1374458709501153290.jpg"
  depositBTCAddress="35UR68XPKRHLDW4nXheGVEYAfSPzBvnVvV"
  tippingQai="10000"
  depositQaiAddress="4TJKs8R55JZEqEe7hFYVJYpQE6CJwGsXAQhSYvF5mS5E"
> <!-- your mml -->
</m-store>
```

![image](https://github.com/user-attachments/assets/420ed1ab-d610-42dc-99e2-220ff39ece7f)

## Store Management

There is a minimum store order management system where the store owner (and storeAdmin) can see a list of valid payments. Note that this is a self-served store infrastructure so store owners need to ship the orders themselves.

## Nakamoto Matrix Holders

We are grateful to build and grow with every one of you! Please join our Discord for guided tours and try out our AI tools to assist you for building your digital worlds on Bitcoin.

## Roadmap

This is a public alpha preview. We’ve been experimenting the best format and structure for building durable digital worlds. With the help of AI, building and growing your dream store would be easier overtime. Here are my work-in-progress items:

- dynamic and real-time live store assets based on Discord/Twitter activities
- integrated text/image-to-3D asset generation pipeline
- custom domains for store owners
- whole store generation with qAI
- NEXT LEVEL upgrades (currently in maintenance mode)
- native multiplayer support in store mode
- spatial qAI APIs with x402 USDC (SOL) payment with $qAI buyback
