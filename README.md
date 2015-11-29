**Fiskus** is a small utility to download transactions in OFX format from various
banks.

Fiskus keeps a cache file to remember when it has been invoked the last time,
and uses this date as starting point to download new transactions.

Usage
-----

Download the transactions since the last run:

    ./fiskus config [cache]

The `config` file includes bank/account information and has the following
format:

```yaml
credentials:
  - bank: CHASE
    login: user
    password: pass

accounts:
  - type: cc
    bank: CHASE
    id: ID
  - type: checkings
    bank: CHASE
    id: ID
  - type: savings
    bank: CHASE
    id: ID
```

Requirements
------------

- Ruby
- [ynab-downloader](https://github.com/glenbot/ynab_downloader)

License
-------

Fiskus comes with 3-clause BSD license.
