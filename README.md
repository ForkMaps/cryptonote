Cryptonote JSON data for [forkmaps.com](https://github.com/jerme404/forkmaps.com).

## Contributing
Coin data is maintained by community contributors.  The easiest way to make a correction or update, or to add a coin, is to do it yourself and submit a PR.  

```bash
# clone 
git clone https://github.com/ForkMaps/cryptonote

# change working directory
cd cryptonote

# install dependencies
npm install

# build
npm run build
```

Each coin has its own JSON file in `src/coins`. A gulp task copies all images in `src/images`, and combines the json files in `src/coins`, using the json file names as object keys.  Output ends up in the `dist` folder.

Forkmaps.com pulls coin data directly from [GitHub](https://github.com/ForkMaps/cryptonote/blob/master/dist/coins.json), so your changes will be live as soon as your PR is merged.


#### Support
```
# BTC
3HLrTJk5fFWRMHipD66TAkcnfWEBmGPmR7

# ETH
0x27b7a2c8cce5bb2b66d01c767632e87145b772ae

# LTC
LaaNvStTVHJ6m3rHx8URG7QMGJiLkN5PJz

# NERVA
NV3Rva5xnA71XrDTxVV7oTJrmNNau9WJucnWBLVwfhtT5TSiUedVEZyigMwXr5kV8q1LHBTLrTBJaYon3qJnrjm31nR2JAE2N

# TRTL
TRTLv1zqKazWXkWHrM1iPuGtyVzGiZJNTboUA7dQcghJhJ8p1v4bx6QM3YjTcAKvJdFswU6qRUdqrKdiCxpDNGHderQpu47tn2N

# XMR
4Cf2TfMKhCgJ2vsM3HeBUnYe52tXrvv8X1ajjuQEMUQ8iU8kvUzCSsCEacxFhEmeb2JgPpQ5chdyw3UiTfUgapJBhAHNczWHnc37Wxn5Mo
```

