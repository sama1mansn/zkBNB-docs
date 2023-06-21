---
title: Overview
---

[zkBNB Marketplace](https://zkbnb-api-testnet.bnbchain.org/) is targeted to be an open-source NFT marketplace for users to browse, buy, sell, or create their own NFT. The meta-data of NFT on zkBNB sticks to the [BSC standard](https://docs.bnbchain.org/docs/nft-metadata-standard/). The ERC721 standard NFT can be seamlessly deposited on zkBNB, or in reverse.

![Marketplace framework](../../../static/img/NFT_Marketplace.png)

The above diagram shows the framework of Nft Marketplace and zkBNB. All the buy/sell offers, meta-data of NFT/Collection, medium resources, and account profiles are stored in the backend of the NFT marketplace, only the **contendHash**, **ownership**, **creatorTreasuryRate**, and a few other fields are recorded on zkBNB. To encourage price discovery, anyone can place a buy/sell offer in the marketplace without paying any fees since the offer is cached in the backend instead of being sent to the zkBNB. Once the offer is matched, an **AtomicMatch** transaction that consists of a buy and sell offer will be sent to zkBNB to make the trade happen. Users can also cancel an offer manually by sending a cancel offer transaction to disable the backend-cached offer.
