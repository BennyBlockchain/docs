# HIVE
Cold Ƀrew is built using the [HIVE](https://hive.io) blockchain. HIVE is a DPoS, graphene blockchain built for handling the high throughput of a social media application. This project currently uses [Hivesigner](https://hivesigner.com) for authentication and [Hive-JS](https://gitlab.syncad.com/hive/hive-js) to communicate with HIVE API's.

## Authentication
Hivesigner is a third party Oauth2 service. Users sign in with their owner key (BIP39 wallet) and create a password for future use and the minting if an access token. The current flow is a lot of redirects and users are signed out when they leave the app. Engagement from the small beta group has gone down since authentication was moved to HIVE.

There are two ways to approach:
1. Improve Hivesigner approach
2. Handle Oauth2 and users private keys in house
3. Verify and sign transactions in app

When considering auth I think it is important to confide to the crypto community which is custody and privacy of keys. Although signing tx's has it's security implications, it alligns with the community the closest.
