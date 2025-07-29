# Resources

## Cowboy TLSN Extension Fork
To get the browser extension on a Chrome-based browser

1. Go to the [Github release](https://github.com/Project-Cowboy/tlsn-extension/releases/tag/cowboy-dev)
2. Click the build.zip.
3. Unzip
4. If on Chrome, go to chrome://extensions/. If on Brave, go to brave://extensions/
5. "Load unpacked"
6. Select the unzipped folder. If it doesn't allow you to upload, you may need to select a build sub-folder.

## Cowboy Prover
To run the local prover which enables proving custom logic developed on Cowboy, please do:

```shell
docker  run -p 1881:1881  ghcr.io/project-cowboy/cowboy-prover:latest ./target/release/k256-example --node-url  "wss://goals-unable-seller-myspace.trycloudflare.com"
```

Leave this running whenever you are using the extension or doing local proving.

## Access the live devnode

To access the live devnode, visit it via the polkadotjs explorer link [here](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Fgoals-unable-seller-myspace.trycloudflare.com)