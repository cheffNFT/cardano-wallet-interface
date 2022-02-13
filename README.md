# cardano-wallet-interface

## Contents
- [Prerequisites](#Prerequisites)
- [Installation](#Installation)
- [Usage](#Usage)
    - [basic usage](#basic_delegation)
        - [nami delegation](#delegate_using_nami)
    - [other examples](#oth_examples)
- [Documentation](#docs_link)
- [Support Harmonic](#Support)

## Prerequisites

make sure to enable web-assembly if not configured by default.

You may find some help at [documentation/known_issues/allowing_webassembly.md](https://github.com/cheffnft/cardano-wallet-interface/blob/main/documentation/known_issues/allowing_webassembly.md)

## Installation

make sure you have a folder called ```node_modules``` in your project

run the following in your project directory

```bash
npm install https://github.com/cheffnft/cardano-wallet-interface
```

## Usage

<a name="basic_delegation">
</a>
<h4>basic delegation functionality</h4>

<a name="delegate_using_nami">
</a>

##### using Nami
```js
/*... other imports ...*/
import Wallet, { WalletName } from "@harmonicpool/cardano-wallet-interface";

/*...*/

if( Wallet.has( WalletName.Nami ) )
{
    if( !Wallet.isEnabled( WalletName.Nami ) )
    {
        Wallet.enable( WalletName.Nami )
        .then(
            () => {
                Wallet.Nami.delegateTo(
                    "<your pool id>",
                    "<your blockforst api key>"
                );
            }
        );
    }
    else
    {
        Wallet.Nami.delegateTo(
            "<your pool id>",
            "<your blockforst api key>"
        );
    }
}

/*...*/
```

<a name="oth_examples">
</a>
<h4>other examples</h4>

check the [documentation/examples](https://github.com/HarmonicPool/cardano-wallet-interface/tree/main/documentation/examples) folder for more

<a name="docs_link">
</a>
<h2>Documentation</h2>

a more in depth documentation can be found in the [documentation folder](https://github.com/cheffnftcheffnft/cardano-wallet-interface/tree/main/documentation)

### Docs Index
- [examples](https://github.com/cheffnft/cardano-wallet-interface/tree/main/documentation/examples)
    - [simple react page using nami](https://github.com/cheffnft/cardano-wallet-interface/blob/main/documentation/examples/SimpleReactPage_Nami.js)
    - [simple react page using ccvault](https://github.com/cheffnft/cardano-wallet-interface/blob/main/documentation/examples/SimpleReactPage_CCVault.js)
- [known issues](https://github.com/HarmonicPool/cardano-wallet-interface/tree/main/documentation/known_issues)
    - [allowing webassembly](https://github.com/cheffnft/cardano-wallet-interface/blob/main/documentation/known_issues/allowing_webassembly.md)
- [Wallet](https://github.com/cheffnft/cardano-wallet-interface/blob/main/documentation/Wallet.md)
- [Errors](https://github.com/cheffnft/cardano-wallet-interface/blob/ma
