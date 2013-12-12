EwayBundle
==========

Symfony2 payment bundle for use with the provider "eWay"


Install
==========


Use
==========

$pay = $this->get('eway');
$pay->setCustomerID("14766081");
$pay->setPaymentAmount("0");
$pay->setCardHoldersName("Regan P Lawton");
$pay->setCardNumber("444433331111222");
$pay->setCardExpiry("03","15");
$pay->setCVN("");

$pay->setCustomerInvoiceDescription("");
$pay->setCustomerInvoiceReference("");
$pay->setCustomerFirstName("Regan");
$pay->setCustomerLastName("Lawton");
$pay->setCustomerEmail("regan@dwd.com.au");
$pay->setCustomerAddress("4/3 Sturt Ter");
$pay->setCustomerPostcode("0870");
$pay->setCustomerTransactionReference("");
$pay->setOption1("");
$pay->setOption2("");
$pay->setOption3("");
$pay->pay();