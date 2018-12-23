# altcoin-genesis
This is just a function that will generate the first transaction of a blockcahin named Genesis
Found in the source of the Pura coin extracted it so that it would be easy to insert it in any altcoin based on Bitcoin.
It is working regardless of the hashing algorithm you are using.

<h1>How to use it?</h1>

1- Copy the function at the top of you chainparams.cpp code.<br>
2- copy the call to the function after the call to CreateGenesisBlock, it should look like this

```
genesis = CreateGenesisBlock(yourtime, yournonce, 0x1d00ffff, 536870912, 50 * COIN); // 536870912 = BIP101
MineGenesis(genesis, consensus.powLimit, true) 
```

Compile and run ./src/qt/yourcoin-qt

It will mine the genesis and display the necessary parameter.
Then you just have to copy/paste the hash, the merkel, the nonce, the time in your genesis, at the right place as described in
Don't forget to comment the call to ManeGenesis once you have modified your chainparams.cpp

The steps to create a basic altcoin with genesis is explained here: https://bitcointalk.org/index.php?topic=3345808.0

<h1>License</h1>

Distributed under the MIT software license. This product includes software developed by the OpenSSL Project for use in the OpenSSL Toolkit. This product includes cryptographic software written by Eric Young (eay@cryptsoft.com), and UPnP software written by Thomas Bernard.
