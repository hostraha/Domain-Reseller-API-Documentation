# API Documentation

## Endpoint
`https://billing.hostraha.com/modules/addons/DomainsReseller/api/index.php`

## Authorization

### Username
This is the email address of the reseller’s client registered in your WHMCS.

### Token
Token is an API Key transformed into SHA256 hash using the reseller’s email address and the current time encoded with base64.

# API Endpoints

## POST - /order/domains/register
**Description:** Register Domain

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text
- **regperiod**
  - Type: numeric
  - Validators: required, numeric
- **domainfields**
  - Type: text
  - Validators: text
- **addons**
  - Type: addons
- **nameservers**
  - Type: nameservers
  - Validators: required
- **contacts**
  - Type: contacts
  - Validators: required

## POST - /order/domains/transfer
**Description:** Transfer Domain

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text
- **eppcode**
  - Type: text
  - Validators: text
- **regperiod**
  - Type: numeric
  - Validators: required, numeric
- **domainfields**
  - Type: text
  - Validators: text
- **addons**
  - Type: addons
- **nameservers**
  - Type: nameservers
  - Validators: required
- **contacts**
  - Type: contacts
  - Validators: required

## POST - /order/domains/renew
**Description:** Renew Domain

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text
- **regperiod**
  - Type: numeric
  - Validators: required, numeric
- **addons**
  - Type: addons

## POST - /domains/{domain}/release
**Description:** Release Domain

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text
- **transfertag**
  - Type: text
  - Validators: required, text

## GET - /domains/{domain}/eppcode
**Description:** Get EPP Code

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text

## GET - /domains/{domain}/contact
**Description:** Get Contact Details

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text

## POST - /domains/{domain}/contact
**Description:** Save Contact Details

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text
- **contactdetails**
  - Type: contactdetails
  - Validators: required

## GET - /domains/{domain}/lock
**Description:** Get Registrar Lock

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text

## POST - /domains/{domain}/lock
**Description:** Save Registrar Lock

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text
- **lockstatus**
  - Type: text
  - Validators: required, text

## GET - /domains/{domain}/dns
**Description:** Get DNS

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text

## POST - /domains/{domain}/dns
**Description:** Save DNS

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text
- **dnsrecords**
  - Type: dnsrecords
  - Validators: required

## POST - /domains/{domain}/delete
**Description:** Request Deletion

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text

## POST - /domains/{domain}/transfersync
**Description:** Transfer Sync

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text

## POST - /domains/{domain}/sync
**Description:** Domain Sync

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text

## GET - /domains/{domain}/email
**Description:** Get Email Forwarding

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text

## POST - /domains/{domain}/email
**Description:** Save Email Forwarding

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text
- **prefix**
  - Type: array
- **forwardto**
  - Type: array

## POST - /domains/{domain}/protectid
**Description:** ID Protect Toggle

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text
- **status**
  - Type: int
  - Validators: required, numeric

## POST - /domains/lookup
**Description:** Check Availability

### Parameters:
- **searchTerm**
  - Type: text
  - Validators: text
- **punyCodeSearchTerm**
  - Type: text
  - Validators: text
- **tldsToInclude**
  - Type: array
  - Validators: isArray
- **isIdnDomain**
  - Type: boolean
- **premiumEnabled**
  - Type: boolean

## POST - /domains/lookup/suggestions
**Description:** Get Domain Suggestions

### Parameters:
- **searchTerm**
  - Type: text
  - Validators: text
- **punyCodeSearchTerm**
  - Type: text
  - Validators: text
- **tldsToInclude**
  - Type: array
  - Validators: isArray
- **isIdnDomain**
  - Type: boolean
- **premiumEnabled**
  - Type: boolean
- **suggestionSettings**
  - Type: array
  - Validators: isArray

## GET - /domains/{domain}/nameservers
**Description:** Get Nameservers

### Parameters:
- **domain**
  - Validators: required, text

## POST - /domains/{domain}/nameservers
**Description:** Save Nameservers

### Parameters:
- **domain**
  - Validators: required, text
- **ns1**
  - Validators: required, text
- **ns2**
  - Validators: required, text
- **ns3**
  - Validators: text
- **ns4**
  - Validators: text
- **ns5**
  - Validators: text

## POST - /domains/{domain}/nameservers/register
**Description:** Register Nameserver

### Parameters:
- **domain**
  - Validators: required, text
- **nameserver**
  - Validators: required, text
- **ipaddress**
  - Validators: required, text

## POST - /domains/{domain}/nameservers/modify
**Description:** Modify Nameserver

### Parameters:
- **nameserver**
  - Validators: required, text
- **currentipaddress**
  - Validators: required, text
- **newipaddress**
  - Validators: required, text

## POST - /domains/{domain}/nameservers/delete
**Description:** Delete Nameserver

### Parameters:
- **nameserver**
  - Validators: required, text

## GET - /order/pricing/domains/{type}
**Description:** Cart Get Pricing

### Parameters:
- **domain**
  - Type: text
  - Validators: required, text

### Scenarios:
- **Register**
- **Renew**
- **Transfer**

## GET - /billing/credits
**Description:** Get Credits

## GET - /version
**Description:** Get Version

## GET - /tlds
**Description:** Get Available TLDs

## GET - /tlds/pricing
**Description:** Get TLDs Pricing

### `/domains/{domain}/information`

**Description:** Get Domain Information

| Field  | Type | Validators            |
|--------|------|-----------------------|
| domain | text | required, text         |

## GET

### `/billing/credits`

**Description:** Get Credits

## GET

### `/version`

**Description:** Get Version

## GET

### `/tlds`

**Description:** Get Available TLDs

## GET

### `/tlds/pricing`

**Description:** Get TLDs Pricing

---
