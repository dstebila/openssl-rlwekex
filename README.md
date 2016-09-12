dstebila/openssl-rlwekex
========================

**OpenSSL** is an open-source TLS/SSL and crypto library ([https://openssl.org/](https://openssl.org/)).  ([View the original README file for OpenSSL](https://github.com/dstebila/openssl-rlwekex/blob/OpenSSL_1_0_1-stable/README).)

This repository contains a **fork of OpenSSL** that adds a key exchange protocol based on the ring learning with errors (ring-LWE) problem from the following paper:

* Joppe W. Bos, Craig Costello, Michael Naehrig, Douglas Stebila. Post-quantum key exchange for the TLS protocol from the ring learning with errors problem. In *Proc. IEEE Symposium on Security and Privacy (S&P) 2015*, pp. 553-570. IEEE, May 2015. DOI:[10.1109/SP.2015.40](http://dx.doi.org/10.1109/SP.2015.40), Eprint <http://eprint.iacr.org/2014/599>.

NOTICE — Migration to new repository (2016/09/12)
-------------------------------------------------

This repository is no longer being updated.  The ring-LWE key exchange code has been incorporated into the [Open Quantum Safe project](https://github.com/open-quantum-safe/).  Open Quantum Safe consists of two portions: 

- [**liboqs**](https://github.com/open-quantum-safe/liboqs), which contains a variety of post-quantum algorithms, including the ring-LWE algorithm from this paper
- a **fork of OpenSSL** ([open-quantum-safe/openssl](https://github.com/open-quantum-safe/openssl)), which adds quantum-safe cryptographic algorithms and ciphersuites via liboqs

If you are interested in an integration of post-quantum key exchange algorithms into OpenSSL, please check out [open-quantum-safe/openssl](https://github.com/open-quantum-safe/openssl).  

This repository
---------------

The modifications in this repository for adding ring-LWE-based ciphersuite appear only on the [OpenSSL\_1\_0\_1-stable branch](https://github.com/dstebila/openssl-rlwekex/tree/OpenSSL_1_0_1-stable).

Note this implementation does not change order of signature in TLS handshake as needed for provable security (see Section 5.1 of the [eprint](http://eprint.iacr.org/2014/599)).

License
-------

All modifications in the `dstebila/openssl-rlwekex` repository are released under the same terms as OpenSSL, namely as described in the file [LICENSE](https://github.com/dstebila/openssl-rlwekex/blob/OpenSSL_1_0_1-stable/LICENSE).  
