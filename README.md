# bitpay-lang

The feature description for any BitPay language core.

## BitPay language cores

BitPay language cores are designated by the name bitpay-\<language\>, for example, "bitpay-python" is the name of the BitPay connector for the python language. Language cores are designed to be easy to use, with simple, descriptive methods and helpful error messages, but this comes at the cost of some functionality. For full functionality in any language, developers can use the library in conjuntion with their own code, the libraries contain all of the methods needed to authenticate with BitPay, retrieve tokens, and generate the cryptographic signatures required to make API requests.

## Language core versions

We are working to extend the language cores to provide simple methods that access every part of the BitPay api. The versioning scheme for language cores is **api version**.**functional spec version**.**patch level**, e.g. `v2.2.1` indicates that the core uses api version 2, meets functional specification 2, and is at patch level 1. The functional specification is described in the the feature files located in the features folder. This spec is written in Gherkin. A developer interested in creating a core that doesn't exist such as Haskell can use the feature files to correctly version their core.

The feature files are tagged per api version and functional specification level.
