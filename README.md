> :warning: This repository has moved :warning:

Solomon is migrating to a monorepo, this repository is no longer used. See https://github.com/solomondefi/solomon-monorepo

# Solomon Blockchain Emailer

A service that scans the blockchain and triggers actions based on incoming log messages. It is intended for use in the Solomon payments
ecosystem, but may be adapted for general use.

At a high level, the operation is simple:
1. Scan blocks for events from a list of contracts
2. On meeting some event condition, e.g. `CreateEscrow` emitted, trigger a list of actions

The list of scanned contracts may be dynamically updated, and actions adhere to a standard plugin interface.

Solomon implements scanners for:
- Notifying (via email) buyers, merchants, or escrow holders when a contract deploys
- Notifying both parties when a dispute is initiated
- Notifying parties when funds are withdrawn from escrow

The service is written with Typescript as a nodejs application. See the [Github
repository](https://github.com/solomondefi/blockchain-mailer) for more technical details including setup and deploy procedures.

## Usage

#### Install

```
npm install
```

#### Develop

```
npm run dev
```

#### Production

```
npm start
```
