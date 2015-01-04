miranda-ssl-openssl
===================

Plugin to provide OpenSSL SslApi to Miranda NG. This requires a Miranda built with
SSL plugin loading support, i.e. 0.95.4 onwards.

Building
--------
1. Clone the Miranda NG [source tree](https://github.com/miranda-ng/miranda-ng).
2. Clone this repository a directory below `$miranda-ng\plugins\`
3. Open the project and add it to the miranda solution (`miranda32.sln`)
4. Build Miranda, then `ssl_openssl_10` (and dependencies). You should receive `Ssl_OpenSSL.dll` in `$miranda-ng\bin10\Release\Plugins\`
5. Copy `Ssl_OpenSSL.dll` to `Plugins` directory and `libeay32.dll` and `ssleay32.dll`
   ([official distribution](https://www.openssl.org/related/binaries.html)) to `Plugins\openssl`.
6. Done! You should now have reasonably good SSL in your Miranda.

Logging
-------
Due to the higher-level API of OpenSSL, logging is not as detailed as with the builtin SSL provider.
The cipher suite used is logged though, so you can search for "SSL established with $foo" to find it.
