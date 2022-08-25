# Pinata Manager
<p align="center">
  <img width="100" src="assets/pinata-manager.png" alt="ipfs action">
</p>

Github action to pin, unpin and update Pinata gateways

The action will automatically update your Pinata's gateway root to be the newly pinned CID.

## Inputs
Param                 | Required |Description
---                   |----------|---
`path`                | Yes      |Path to file or directory you want to pin
`secret`              | Yes      |Your Pinata secret
`key`                 | Yes      |Your Pinata API key
`token`               | Yes      |Your Pinata JWT
`pinName`             | Yes      |Name of the pinned file. Default `super cool ipfs pin`
`unpinOld`            | No       |Whether or not to unpin an older pin with the same name. Default `false`
`gatewayName`         | Yes      |The name of your target gateway. **Note:** This _must_ be setup in your Pinata dashboard before using this action!
`gatewayId`           | Yes      |The Id of your target gateway. **Note:** You have to extract this from your Pinata dashboard by opening the network monitor and setting _any_ file as gateway root.

## Outputs

- `gateway` - Returns the new gateway address of a successful pin
- `cid` - Returns the CID of the built codebase
- `duplicate` - Returns true if the pin was skipped
