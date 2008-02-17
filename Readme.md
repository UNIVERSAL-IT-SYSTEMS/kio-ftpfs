KIO FTPS Slave
===

*Note:* This project has been unmaintained for a long time, it is hosted for archive purposes.

kio-ftps is an FTPS KIO slave for KDE. It implements secure FTP sessions based on RFC 4217 and built upon the FTP KIO-slave sources. It should work with most server implementations. It issues an `AUTH TLS` command after connecting and refuses to continue when it's not supported. Prior to every data channel I/O command (`STOR`, `RETR`, etc.) it tries to secure the data channel via `PBSZ` and `PROT` commands. If that fails, it will transfer data unencrypted.

It currently supports:

  - Control channel encryption.
  - Encrypted PASV data transfers.

It lacks:

  - Authentification via client certificate.
  - Encrypted PORT data transfers.
