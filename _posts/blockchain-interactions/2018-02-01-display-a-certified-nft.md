---
date: 2018-02-07
title: Display an NFT in a scene
description: Learn how to display a certified NFT that you own in your scene
categories:
  - blockchain-interactions
type: Document
set: blockchain-interactions
set_order: 4
---

In future versions of the SDK, it will be possible to display an NFT (Non-Fungible Token) that you own in your Decentraland scenes. A glowing badge will appear above the NFT to certify that you indeed own it.

This feature is not currently supported, but is on the roadmap.

> Note: As a workaround, if you want to display a token you can obtain an NFT image from [OpenSea's API](https://docs.opensea.io/reference#api-overview) and set that as a texture for a material. Then you can use that material on any primitive object in the scene.	


<!--
You can display an NFT (Non-Fungible Token) that you own in your Decentraland scenes. A glowing badge will appear above the NFT to certify that you indeed own it.

<img src="/images/media/verified-nft.png" alt="nested entities" width="300"/>

> Note: The NTF's image data is taken from the [OpenSea](https://opensea.io/) API, based on the token's contract and id. Note that most images from the OpenSea API are 2D, but categories like [Chainbreakers](https://opensea.io/assets/chainbreakerspresale) will return 3D assets.

## Add an NFT

Add an `NFTShape` component to an entity to display a 2D token in your scene.

```ts
// create entity
const nft = new Entity()

// position entity
nft.addComponent(new Transform({
  position: new Vector3(1, 1.2, 1)
  }))

// add an NFTShape, instanced with a token contract and token id
nft.addComponent(new NFTShape("0x06012c8cf97bead5deae237070f9587f8e7a266d", "475577"))

// add entity to engine
engine.addEntity(nft)
```

The `NFTShape` component must be instanced with two parameters:

- The _contract_ of the token (for example, the CryptoKitties contract)
- The _id_ of the specific token you own

When the token is displayed, it's shown as a plane object. Its texture is shadeless, like a basic material.

## Token certification

When using the `NFTShape` component, the engine automatically runs a verification. The same Ethereum wallet that owns the LAND tokens where the scene is deployed must also own the token.

If you don't own the token, the image isn't displayed in the scene.

This verification is carried out by users loading your scene, every time the entity with the `NFTShape` component is added to the engine.

Above the image of the token, we display a badge that certifies its authenticity. The badge glows in a pulsating pattern, providing a stamp that is difficult to falsify.
-->
