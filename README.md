# Catenis Message Inspector Web App

A web application used for exploring the data structures that comprise a Catenis message.

## Design

This web application has been designed as a single HTML page, making use of [Bootstrap](https://getbootstrap.com) for the UI and the
 [catenis-msg-inspector](https://github.com/blockchainofthings/catenis-msg-inspector) JavaScript library to actually
 perform the inspection of the Catenis message.

### Browser compatibility

The web application's HTML page is compatible with modern web browsers.

It has been tested on the following web browsers:

- Safari ver. 13.1 (on macOS Catalina 10.15)
- Google Chrome ver. 83.0 64 bits (on macOS Catalina 10.15, Windows 10)
- Google Chrome ver. 83.0 32 bits (on Windows 8.1)
- Firefox ver. 76.0 64-bits (on macOS Catalina 10.15)
- Microsoft Edge ver. 44 (on Windows 10)

> **Note**: Internet Explorer is **not** supported.

## Deployment

To deploy this web application, just copy the `ctn-msg-inspector.html` HTML page along with the `assets` directory and its contents to a
 web server.

## Usage

The page has two input fields, namely `Transaction ID` and `Off-Chain CID`.

To inspect a Catenis message, one must have information about the message's container, which should be obtained by
 calling the [Retrieve Message Container](https://catenis.com/docs/api/0.9/#retrieve-message-container) method of the
 Catenis API.

The value of the `blockchain.txid` property of the returned message container info should then be entered into the
 `Transaction ID` input field, whereas the value of the `offChain.cid` property should be entered into the
  `Off-Chain CID` input field.

### Inspecting standard Catenis messages

To inspect standard Catenis messages, only the `Transaction ID` should be provided.

### Inspecting off-chain Catenis messages

To inspect off-chain Catenis messages, either or both the `Transaction ID` and the `Off-Chain CID` can be provided.

When the `Transaction ID` is provided, the inspection will include information about the settlement of
 the message on the blockchain.

In contrast, when the `Off-Chain CID` is provided, the inspection will reveal information about the message itself.

## License

This web application is released under the [MIT License](LICENSE). Feel free to fork, and modify!

Copyright © 2020, Blockchain of Things Inc.