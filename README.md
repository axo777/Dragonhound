# Dragonhound
GPS tracking a wandering hound with Particle.io via Komodo cryptoconditions oracles, displayed on Leaflet


This app is designed to display GPS coordinates on a map in a web browser. 

The current version reads the coordinates from readings published over 3G via Particle.io, using an Asset Tracking kit.

This data is encrypted, and then written into a Komodo asset chain via a cryptoconditions oracle (smart contract) though a blockchain transaction.

The asset chain oracle acts to store coordinate history, without compromising the location intelligence of the user (unlike other commercial mapping services who claim not to be evil).

When loading the map in your browser, the app queries the asset chain oracle, decrypts the stored coordinates, and displays them on the map.

Each interaction with the oracle requires an on chain transaction of nominal value, so to create a user oracle and query the data within, the account will need to be funded.

While in testing, you can fund your account with 1 KMD, which will be converted into enough tokens to cover thousands of oracle interactions for whichever asset chain your oracle is created on.

Half of any KMD recieved will fund further development, and half will be applied to various community bounties listed on dragonhound.tech

---------------------------------------------------
The current version is single user only, using cherry py framework. 
The version in development allows multiple users, and is using django framework.
---------------------------------------------------

Assets used
- Leaflet (for mapping)
- Komodo Platform (to fund user accounts)
- KMD Labs (for testing oracle and other cryptoconditions implementations)
- Particle.io (GPS Asset tracking hardware)
- Particle cloud (middleware to get data from device to oracle)
