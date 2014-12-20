miranda-ssl-openssl
===================

Core Plugin to provide OpenSSL SslApi to (patched) Miranda NG. This requires a Miranda built with
SSL plugin loading support, i.e. [this branch](https://github.com/martok/miranda-ng/tree/sslapi).

Building
--------
1. Clone the Miranda NG [source tree](https://github.com/miranda-ng/miranda-ng).
2. Clone this repository a directory below `$miranda-ng\src\core\`
3. Open the project and either add it to the miranda solution or save a new one in the same directory as miranda32.sln
4. Build `sslapi_openssl_10` (and dependencies). You should receive `SslApi_OpenSSL.dll` in `$miranda-ng\bin10\Core\`
5. Copy `SslApi_OpenSSL.dll` with `libeay32.dll` and `ssleay32.dll` ([official distribution](https://www.openssl.org/related/binaries.html))
   to your the subdirectory `Core` (*not* `Plugins`!) of your Miranda installation path.
6. Done! You should now have reasonably good SSL in your Miranda.

Logging
-------
Due to the higher-level API of OpenSSL, logging is not as detailed as with the builtin SSL provider.
The cipher suite used is logged though, so you can search for "SSL established with $foo" to find it.
