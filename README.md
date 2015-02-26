# bitpay-lang

The feature description for any BitPay language core.

## BitPay

BitPay is a bitcoin and blockchain technology company that offers a variety of services including merchant payment processing. The core language libraries and shopping cart plugins are targeted to provide access to BitPay's merchant processing API.

A complete description of the BitPay API is out of scope for this document, but the API Version 2 documentation is [available on BitPay's site](https://bitpay.com/api).

## Authentication

In order to use the API at all, a developer has to access BitPay authentication through the BitAuth protocol. Making this protocol easy to use is a key function of the language cores.

## BitPay language cores

BitPay language cores are designated by the name bitpay-\<language\>, for example, "bitpay-python" is the name of the BitPay connector for the python language. Language cores are designed to be easy to use, with simple, descriptive methods and helpful error messages, but this comes at the cost of some functionality. For full functionality in any language, developers can use the library in conjuntion with their own code, the libraries contain all of the methods needed to authenticate with BitPay, retrieve tokens, and generate the cryptographic signatures required to make API requests.

## Language core versions

We are working to extend the language cores to provide simple methods that access every part of the BitPay api. The versioning scheme for language cores is **api version**.**functional spec version**.**patch level**, e.g. `v2.2.1` indicates that the core uses api version 2, meets functional specification 2, and is at patch level 1. The functional specification is described in the the feature files located in the features folder. This spec is written in Gherkin. A developer interested in creating a core that doesn't exist such as Haskell can use the feature files to correctly version their core.

The feature files are tagged per api version and functional specification level.

## Request Syntax

BitPay API endpoints can generally be accessed through either `get` or `create` methods. For example, in ruby, the method `create_invoice(params)` will generate a POST message to the '/invoices' endpoint with whatever parameters you pass into the method.

Similary, `get_invoice` will send a GET request to the '/invoices' endpoint with the arguments that you inlcude. `get_invoice_by_id` will send a GET request to the '/invoices/\<id\>' endpoint, where id is an `id` parameter that you pass into the method. The `by` syntax can be reused, e.g. `get_invoice_by_id_by_events`.

A point of potential confusion: all method names are singular, all endpoints are not. To send a request to the '/payouts' endpoint, you use the method `get_payout`, not `get_payouts`. We may improve this to accept either in a future release.

Method names follow the convention of the language. Equivalent methods in Php are named `getInvoice` or `createInvoice`.
