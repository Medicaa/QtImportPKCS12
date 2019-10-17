# QtImportPKCS12

This is a Qt application that demonstrates reading a PKCS#12 (.pfx or p12 file).
The program is designed to work on Windows, Linux, Android, macOS and iOS.

This program demonstrates how to workaround a known limitation in `QSslCertificate::importPkcs12`
on macOS, iOS by linking directly to OpenSSL.

## Building

This Qt application was developed and tested with Qt 5.13.1 and OpenSSL 1.1.1d.
For macOS and iOS, you will need to build OpenSSL from source code.
For all other platforms, OpenSSL is part of the default Qt kits.

### Building OpenSSL for iOS

To build OpenSSL for iOS:

```bash
cd scripts
./build_openssl_ios.sh
```

### Building OpenSSL for macOS

To build OpenSSL for macOS:

```bash
cd scripts
./build_openssl_macos.sh
```

## Running the Qt Application

To run the application, you will need access to a PKCS#12 file (usually a .pfx or a .p12)
that contains a private key, certificates, and, optionally, CA certificates.

You may need to specify a passphrase to unlock the PKCS#12 file.

When unlocked, it will display whether it has detected the private key, certificate and
CA certificates.
