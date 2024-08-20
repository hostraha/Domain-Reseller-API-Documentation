# API Documentation

## Endpoint
`https://billing.hostraha.com/modules/addons/DomainsReseller/api/index.php`

## Authorization

### Username
This is the email address of the reseller’s client registered in your WHMCS.

### Token
Token is an API Key transformed into SHA256 hash using the reseller’s email address and the current time encoded with base64.

```php
base64_encode(hash_hmac("sha256", "<api-key>", "<email>:<gmdate("y-m-d H")>"))
