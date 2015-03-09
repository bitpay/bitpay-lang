<?php
# BitPay Client

## Authentication and Instantiation
```php
\Bitpay\Client::__construct($options = null)
$options = array(
    'host'   => 'test.bitpay.com',
    'key'    => '**PEM_ENCODED_FILE**',
    'tokens' => array(
        array(
            'token' => 'dsfhkdasjhfjhasdjfhsdkjaf',
            'facade'   => 'pos'
        ),
        array(
            'token' => 'faslkdjalksdjflkjasdkfjld',
            'facade'   => 'merchant'
        ),
        array(
            'token' => 'oeuwroiweuskdfjlasjdflkaie',
            'facade'   => 'merchant-invoice'
        )
    )
)
```

## Resources
```php
// Invoices
\Bitpay\Client->createInvoice($invoice)
\Bitpay\Client->getInvoice($invoice_id)
\Bitpay\Client->getInvoiceEvents($invoice_id)
\Bitpay\Client->listInvoices($options = null)
\Bitpay\Client->refundInvoice($invoice_id, $refund)
\Bitpay\Client->getInvoiceRefund($invoice_id, $refund_id)
\Bitpay\Client->cancelInvoiceRefund($invoice_id, $refund_id)
\Bitpay\Client->adjustInvoice($invoice_id, $adjustment)
\Bitpay\Client->resendInvoiceNotification($invoice_id)

// Rates
\Bitpay\Client->listRates()
\Bitpay\Client->getRate($currency)

// Tokens
\Bitpay\Client->createToken($token)
\Bitpay\Client->setToken($token)
\Bitpay\Client->setTokens($tokens[])
\Bitpay\Client->listTokens()
```