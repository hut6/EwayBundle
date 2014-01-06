EwayBundle
==========

Symfony2 payment bundle for use with the provider "eWay"


Install
==========

Enable the bundle in the kernel:

``` php
<?php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...
        new Hut6\Eway\PaymentBundle\EwayPaymentBundle(),
    );
}
```

Use
==========

All fields are required, however not all are required byway and can be blank.

```
$pay = $this->get('eway');
$pay->setCustomerID("XXXXXXXX");
$pay->setPaymentAmount("0");
$pay->setCardHoldersName("John P Smith");
$pay->setCardNumber("444433331111222");
$pay->setCardExpiry("MM","YY");
$pay->setCVN("XXX");

$pay->setCustomerInvoiceDescription("");
$pay->setCustomerInvoiceReference("");
$pay->setCustomerFirstName("");
$pay->setCustomerLastName("");
$pay->setCustomerEmail("");
$pay->setCustomerAddress("");
$pay->setCustomerPostcode("");
$pay->setCustomerTransactionReference("");
$pay->setOption1("");
$pay->setOption2("");
$pay->setOption3("");
$pay->pay();

```

All fields are required, however not all are required byway and can be blank.

``` yml
// app/config/config.php
services:
    // ...
    eway:
        class: Hut6\Eway\PaymentBundle\EwayPaymentBundle

```