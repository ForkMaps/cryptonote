# cryptonote-tree-json
Cryptonote JSON data for [forkmaps.com](https://github.com/jerme404/forkmaps.com).

## Contributing
Coin data is maintained by community contributors.  The easiest way to make a correction or update, or to add a coin, is to do it yourself and submit a PR.  

### Get the project
Clone the repository.
```bash
git clone https://github.com/jerme404/forkmaps-json-cryptonote
cd cryptonote-tree-json
```
Install dependencies.
```bash
npm install
```

### Make your changes
Each coin has its own JSON file in `src/coins`.

### Build
A gulp task copies all images in `src/images`, and combines the json files in `src/coins`, using the json file names as object keys.  Output ends up in the `dist` folder.

Build with
```bash
npm run build
```

The website pulls coin data from [GitHub](https://github.com/jerme404/forkmaps-json-cryptonote/blob/master/dist/coins.json), so your changes will be live as soon as your PR is merged.
