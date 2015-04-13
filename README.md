# php-bitcoin-address-validator

A simple, easy to use PHP StartCOIN address validator

## Usage

Quick start:

```php
use \StartCOIN\AddressValidator;

// This will return false, indicating invalid address.
AddressValidator::isValid('blah');

// This is a valid address and will thus return true.
AddressValidator::isValid('sWzkFZhn2S9hDrcwr9me5XQezFs2x5dP8d');

// This is a Testnet address, it's valid and the function will return true.
AddressValidator::isValid('tLCB14RsgKctcRx8XeTdZDBbdLELDa6kft', AddressValidator::TESTNET);
```

## API

### `isValid($addr, $version)`

- `$addr`: A StartCOIN address
- `$version`: The version to test against, defaults to `MAINNET`

Returns a boolean indicating if the address is valid or not.

### `typeOf($addr)`

- `$addr`: A StartCOIN address

Returns the type of the address.

## Constants

The library exposes the following constants.

- `MAINNET`: Indicates any mainnet address type
- `TESTNET`: Indicates any testnet address type
- `MAINNET_PUBKEY`: Indicates a mainnet pay to pubkey hash address
- `MAINNET_SCRIPT`: Indicates a mainnet pay to script hash address
- `TESTNET_PUBKEY`: Indicates a testnet pay to pubkey hash address
- `TESTNET_SCRIPT`: Indicates a testnet pay to script hash address
