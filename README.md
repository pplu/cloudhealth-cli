CloudHealth CLI
===============

A CLI for the CloudHealth API

Installing
==========

 - Build the container with the CLI `make container` in this repo

```
git clone git@github.com:pplu/cloudhealth-cli.git
cd cloudhealth-cli
make container
```

It's convenient to define an alias for the `cloudhealth-cli` command:

```
alias cloudhealth-cli="docker run -eCLOUDHEALTH_APIKEY=$(echo \$CLOUDHEALTH_APIKEY) --rm cloudhealth-cli"
```

 - The CLI is also available via CPAN if you want to install it in your local system via the usual Perl Toolchain (cpan/cpanm/cpm, etc)

```
cpanm CloudHealth::CLI
```

Running it
==========

First you need an API Key to authenticate to the API. This can be found in the CloudHealth control panel, under your user profile, in the API Key section.

```
export CLOUDHEALTH_APIKEY=xxx
```

```
cloudhealth-cli
```
Will show a help with the commands available:

```
cloudhealth-cli AWSAccounts
```
Will run the AWSAccounts command

```
cloudhealth-cli AWSAccounts help
```

Will show that the AWSAccounts command accepts the `page` and `per_page` parameters:

```
cloudhealth-cli AWSAccounts page 2
```

Will pass "2" as the value of the page parameter of AWSAccounts

Copyright
=========

(c) 2018 CAPSiDE SL

Author
======

Jose Luis Martinez Torres
