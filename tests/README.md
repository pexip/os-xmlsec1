# XMLSec Library: Unit Tests

## Running a specific test

If a test fails, it's possible to re-run just that specific test for that
specific backend using:

```
make check-crypto-$backend XMLSEC_TEST_NAME="$name"
```

where `$name` is the key name for key tests, and a file name otherwise.

Example:

```
make check-crypto-nss XMLSEC_TEST_NAME="enveloping-sha256-rsa-sha256-relationship"
```

## Reproducible output

It is also possible to have reproducible output, filtering out timestamps. This
is useful to see the output before and after a change to understand its impact.

Example:

```
make check-crypto-nss XMLSEC_TEST_REPRODUCIBLE=y
```
