Cryptonote JSON data for [forkmaps.com](https://github.com/jerme404/forkmaps.com).

## Contributing
Coin data is maintained by community contributors.  The easiest way to add or update coin data is to do it yourself, and submit a PR.  

```bash
# clone
git clone https://github.com/ForkMaps/cryptonote

# change working directory
cd cryptonote

# install dependencies if you want to build/validate your changes
npm install

# build
npm run build
```

Each coin has its own JSON file in `src/coins`. A gulp task copies all images in `src/images`, and combines the json files in `src/coins`, using the json file names as object keys.  Output ends up in the `dist` folder.

### Coin Files

Coin JSON files should be name using both the coin ticker symbol, and the coin name, using this format: `ticker-name.json`.  So the Monero file is `xmr-monero.json`.  This keeps forks easy to reference, and helps prevent duplicate coin keys.

Before submitting a pull request, please either run your changes through a JSON validator, or run `npm run build` to make sure you JSON is properly formatted. 

Use this JSON template
```json
{
    "algorithm": "pow algorithm - REQUIRED",
    "coin": "coin ticker symbol - REQUIRED",
    "endDate": "dead coin end date, format YYYY-MM-DD or YYYY-MM",
    "forkedFrom": "coin this was forked from - REQUIRED",
    "icon": "link to coin icon",
    "links": {
        "bitcointalkAnn": "bitcointalk.org announcement thread",
        "discord": "discord link",
        "facebook": "facebook page",
        "reddit": "reddit link",
        "repo": "code repository, project, or organization - REQUIRED",
        "telegram": "telegram link",
        "twitter": "twitter link",
        "website": "coin website"
    },
    "name": "coin name - REQUIRED",
    "startDate": "coin launch date, format YYYY-MM-DD or YYYY-MM"
}
```

**Note on forkedFrom:** If the project came from [cryptonotefoundation](https://github.com/cryptonotefoundation/cryptonote) or [forknote](http://forknote.net/create/#/), use `"forkedFrom": "bcn-bytecoin"`.

### Images

The easiest way to add a coin icon is to add it to the `src/images` folder, and then reference in that coin's JSON file with `"icon": "https://storage.googleapis.com/forkmaps/images/cryptonote/COIN_ICON_NAME.png"`. 

If you want the icon to look good on the site, please use a quality, cropped image (meaning, no padding around it) with a transparent background, and a reasonable file size.

### Adding Coins

To add a coin, either create a new json file in `src/coins` using the coin ticker symbol, and the coin name.  So the file name format should be `ticker-name.json`.  Copy the JSON template above, enter your data, and delete the properties you don't use.

### Updating Coins

To update a coin, find the JSON file in `src/coins` for the coin you want to update, make your changes, and submit a pull request.

Forkmaps.com pulls coin data directly from [GitHub](https://github.com/ForkMaps/cryptonote/blob/master/dist/coins.json), so your changes will be live as soon as your PR is merged.


#### Support
All donations go to the community, in the form of giveaways, tips, and bounties.
```
# BTC 3HLrTJk5fFWRMHipD66TAkcnfWEBmGPmR7
# ETH 0x27b7a2c8cce5bb2b66d01c767632e87145b772ae
# LTC LaaNvStTVHJ6m3rHx8URG7QMGJiLkN5PJz
# NERVA NV3Rva5xnA71XrDTxVV7oTJrmNNau9WJucnWBLVwfhtT5TSiUedVEZyigMwXr5kV8q1LHBTLrTBJaYon3qJnrjm31nR2JAE2N
# TRTL TRTLv1zqKazWXkWHrM1iPuGtyVzGiZJNTboUA7dQcghJhJ8p1v4bx6QM3YjTcAKvJdFswU6qRUdqrKdiCxpDNGHderQpu47tn2N
# XMR 4Cf2TfMKhCgJ2vsM3HeBUnYe52tXrvv8X1ajjuQEMUQ8iU8kvUzCSsCEacxFhEmeb2JgPpQ5chdyw3UiTfUgapJBhAHNczWHnc37Wxn5Mo
```
