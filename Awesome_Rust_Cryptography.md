# Short URL for this page: [cryptography.rs](https://cryptography.rs)

<img align="right" height="100px" src="https://raw.githubusercontent.com/The-DevX-Initiative/RCIG_Coordination_Repo/main/mascot.png">

<img align="right" height="100px" src="https://raw.githubusercontent.com/The-DevX-Initiative/RCIG_Coordination_Repo/main/RCIG_Mascot3.png">
Below is a list of actively maintained, high-quality cryptography libraries
independently developed by members of the Rust Community.

The list is compiled and curated by the
[Rust Cryptography Interest Group (RCIG)](https://github.com/The-DevX-Initiative/RCIG_Coordination_Repo).
If you have any suggestions, questions, or other concerns with this list,
please
[open an issue](https://github.com/The-DevX-Initiative/RCIG_Coordination_Repo/issues/new?title=Awesome+Rust+Cryptography:+[issue+here])
and we'll get back to you.

The following badges are used to provide more information about libraries
that meet certain criteria:

| Badge               | Description |
|---------------------|-------------|
| ![][audited-badge]  | crate has at least one security audit (click to view)  |
| ![][verified-badge] | crate has been formally verified |

Note: libraries in each section are listed in alphabetical order, *not* order
of preference.

[audited-badge]: https://img.shields.io/badge/audited-success.svg
[verified-badge]: https://img.shields.io/badge/verified-informational.svg

## Table of Contents

- [High-level Libraries](#high-level-libraries)
- [Transport Encryption Libraries](#transport-encryption-libraries)
- [Collections of Cryptographic Primitives](#collections-of-cryptographic-primitives)
- [Traits for Cryptographic Primitives](#traits-for-cryptographic-primitives)
- [Symmetric Cryptography](#symmetric-cryptography)
- [Asymmetric Cryptography](#asymmetric-cryptography)
- [Platform / Framework Bindings](#platform--framework-bindings)
- [Cryptographic Hardware](#cryptographic-hardware)
- [Post-Quantum Cryptography](#post-quantum-cryptography)
- [Random Number Generators](#random-Number-generators)
- [Zero-knowledge Proofs](#zero-knowledge-proofs)
- [Secure Multiparty Computation](#secure-multiparty-computation)
- [Fully Homomorphic Encryption](#fully-homomorphic-encryption)
- [Format Decoders/Encoders](#format-decodersencoders)
- [Defensive Measures](#defensive-measures)
- [Arithmetic](#arithmetic)
- [Miscellany](#miscellany)

## High-level Libraries

[up](#table-of-contents)

These libraries function at a very high level and are designed for simplicity
and ease-of-use. They provide integrated key management in addition to
providing high-level APIs for algorithms.

- [rage](https://github.com/str4d/rage) Implementation of
 [age](https://age-encryption.org/) -- a simple, secure and modern encryption
 tool with small explicit keys, no config options, and UNIX-style
 composability.

- [signatory](https://github.com/iqlusioninc/crates/tree/main/signatory)
 High-level digital signature library with support for ECDSA and Ed25519.

- [tink-rust](https://github.com/project-oak/tink-rust) Rust port of Google's
 high-level Tink cryptography library.

## Transport Encryption Libraries

[up](#table-of-contents)

These libraries implement protocols that are designed to protect
data-in-transit; i.e., network communications.

- [rustls](https://github.com/ctz/rustls)
 [![][audited-badge]](https://cure53.de/pentest-report_rustls.pdf)
 Modern SSL/TLS library in Rust.

- [snow](https://github.com/mcginty/snow) Pure Rust implementation of Trevor
 Perrin's [Noise Protocol](https://noiseprotocol.org).

- [strobe-rs](https://github.com/rozbb/strobe-rs) Relatively barebones,
 `no_std` implementation of the [Strobe protocol
 framework](https://strobe.sourceforge.io/) in pure Rust.

- [OpenMLS](https://github.com/openmls/openmls/)
 [MLS](https://datatracker.ietf.org/doc/draft-ietf-mls-protocol/)
 implementation in Rust.

- [webpki](https://github.com/briansmith/webpki) validates Web PKI (TLS/SSL)
 certificates

## Collections of Cryptographic Primitives

[up](#table-of-contents)

These libraries provide omnibus collections of different cryptographic
primitives contained within a single library.

- [evercrypt-rust](https://github.com/franziskuskiefer/evercrypt-rust)
 ![][verified-badge] Rust bindings for
 [evercrypt](https://github.com/project-everest/hacl-star/tree/master/providers/evercrypt),
 a set of high-performance HACL\*-verified implementations of cryptographic
 primitives. bindings crate, bringing HACL-verified cryptographic primitives.

- [libsm](https://github.com/citahub/libsm) China's Standards of Encryption
 Algorithms (SM2/3/4).

- [orion](https://github.com/brycx/orion) Collection of usable, easy and safe
 pure-Rust cryptographic primitives.

- [\*ring\*](https://github.com/briansmith/ring)
 [![][audited-badge]](https://cure53.de/pentest-report_rustls.pdf)
 focused on the implementation, testing, and optimization of a core set of
 cryptographic operations exposed via an easy-to-use (and hard-to-misuse)
 API. \*ring\* exposes a Rust API and is written in a hybrid of Rust, C, and
 assembly language.

- [themis](https://github.com/cossacklabs/themis) Cross-platform general
 purpose crypto library for securing data during authentication, storage,
 messaging, network exchange, etc.

- [dryoc](https://github.com/brndnmtthws/dryoc) A pure-Rust, general purpose
 crypto library that implements libsodium primitives.

## Traits for Cryptographic Primitives

[up](#table-of-contents)

The crates in this section provide trait-based abstractions for different types
of cryptographic primitives, allowing implementations of higher-level
cryptographic algorithms and protocols which are generic over specific
primitives and implementations.

- [aead](https://github.com/RustCrypto/traits/tree/master/aead) Authenticated
 Encryption with Additional Data (AEAD) cipher traits.

- [ark-ec](https://github.com/arkworks-rs/algebra/tree/master/ec) Elliptic
 curve traits as used by the [`arkworks` ecosystem](arkworks.rs).

- [ark-ff](https://github.com/arkworks-rs/algebra/tree/master/ff) Finite
 field traits as used by the [`arkworks` ecosystem](arkworks.rs).

- [cipher](https://github.com/RustCrypto/traits/tree/master/cipher) Block
 cipher and stream cipher traits.

- [crypto](https://github.com/RustCrypto/traits/tree/master/crypto) Facade
 for all [RustCrypto](https://github.com/RustCrypto) traits.

- [crypto-mac](https://github.com/RustCrypto/traits/tree/master/crypto-mac)
 Message Authentication Code (MAC) traits.

- [digest](https://github.com/RustCrypto/traits/tree/master/digest)
 Digest/hash algorithm traits.

- [elliptic-curve](https://github.com/RustCrypto/traits/tree/master/elliptic-curve)
 Elliptic curve traits as used by the RustCrypto ecosystem.

- [ff](https://github.com/zkcrypto/ff) Finite field traits as used by the
 RustCrypto and ZKCrypto ecosystems.

- [group](https://github.com/zkcrypto/group) Elliptic curve group traits as
 used by the RustCrypto and ZKCrypto ecosystems.

- [pairing](https://github.com/zkcrypto/pairing)
 Pairing-friendly curve traits as used by the ZKCrypto ecosystem.

- [password-hash](https://github.com/RustCrypto/traits/tree/master/password-hash)
 Password hashing traits and support for the PHC string format.

- [signature](https://github.com/RustCrypto/traits/tree/master/signature)
 Digital signature traits.

- [universal-hash](https://github.com/RustCrypto/traits/tree/master/universal-hash)
 Universal Hash Function (UHF) traits.

## Symmetric Cryptography

[up](#table-of-contents)

These crates implement individual symmetric cryptography algorithms.

### Authenticated Encryption with Associated Data (AEAD) Algorithms

These are high-level symmetric encryption libraries which ensure both the
confidentiality and integrity of data.

- [aes-gcm](https://github.com/RustCrypto/AEADs/tree/master/aes-gcm)
 [![][audited-badge]](https://research.nccgroup.com/2020/02/26/public-report-rustcrypto-aes-gcm-and-chacha20poly1305-implementation-review/)
 Pure Rust implementation of the AES-GCM Authenticated Encryption with
 Associated Data (AEAD) cipher.

- [aes-gcm-siv](https://github.com/RustCrypto/AEADs/tree/master/aes-gcm-siv)
 AES-GCM-SIV (RFC 8452) is a state-of-the-art high-performance Authenticated
 Encryption with Associated Data (AEAD) cipher which also provides nonce
 reuse misuse resistance.

- [aes-siv](https://github.com/RustCrypto/AEADs/tree/master/aes-siv) AES-SIV
 Misuse-Resistant Authenticated Encryption Cipher.

- [ccm](https://github.com/RustCrypto/AEADs/tree/master/ccm) Pure Rust
 implementation of the Counter with CBC-MAC (CCM) mode (RFC 3610): an
 Authenticated Encryption with Associated Data (AEAD) algorithm generic over
 block ciphers with block size equal to 128 bits.

- [chacha20poly1305](https://github.com/RustCrypto/AEADs/tree/master/chacha20poly1305)
 [![][audited-badge]](https://research.nccgroup.com/2020/02/26/public-report-rustcrypto-aes-gcm-and-chacha20poly1305-implementation-review/)
 Pure Rust implementation of ChaCha20Poly1305 (RFC 8439): an Authenticated
 Encryption with Associated Data (AEAD) cipher amenable to fast,
 constant-time implementations in software.

- [deoxys](https://github.com/RustCrypto/AEADs/tree/master/deoxys) Pure Rust
 implementation of the Deoxys Authenticated Encryption with Associated Data
 (AEAD) cipher, including the Deoxys-II variant which was selected by the
 CAESAR competition as the best choice for in-depth security.

- [eax](https://github.com/RustCrypto/AEADs/tree/master/eax) Pure Rust
 implementation of the EAX Authenticated Encryption with Associated Data
 (AEAD) cipher.

### Ciphers (low-level block ciphers and stream ciphers)

Note: most users should use higher-level AEAD encryption algorithms
enumerated above.  Crates in this section are low-level "unauthenticated"
ciphers which should be wrapped up in a higher-level construction prior to
use.

- [aes](https://github.com/RustCrypto/block-ciphers/tree/master/aes)
 [![][audited-badge]](https://research.nccgroup.com/2020/02/26/public-report-rustcrypto-aes-gcm-and-chacha20poly1305-implementation-review/)
 Pure Rust implementation of the Advanced Encryption Standard (AES)
 permutation with optional AES-NI and ARMv8 hardware acceleration.

- [block-modes](https://github.com/RustCrypto/block-modes)
 Generic implementation of block cipher modes of operation, including CBC and
 ECB modes.

- [chacha20](https://github.com/RustCrypto/stream-ciphers/tree/master/chacha20)
 [![][audited-badge]](https://research.nccgroup.com/2020/02/26/public-report-rustcrypto-aes-gcm-and-chacha20poly1305-implementation-review/)
 Pure Rust implementation of the ChaCha20 Stream Cipher including XChaCha20.

- [ctr](https://github.com/RustCrypto/stream-ciphers/tree/master/ctr) Generic
 implementations of the Counter Mode (CTR) of operation for block ciphers.

- [des](https://github.com/RustCrypto/block-ciphers/tree/master/des)  Data
 Encryption Standard (DES) and 3DES.

- [salsa20](https://github.com/RustCrypto/stream-ciphers/tree/master/salsa20)
  Pure Rust implementation of the Salsa20 Stream Cipher.

### Hash Functions and Friends

- [BLAKE2](https://github.com/RustCrypto/hashes/tree/master/blake2) Pure Rust
 implementation of the BLAKE2 hash function family.

- [BLAKE3](https://github.com/BLAKE3-team/BLAKE3) Official implementation of
 the BLAKE3 cryptographic hash function.

- [HKDF](https://github.com/RustCrypto/KDFs/tree/master/hkdf) HMAC-based
 Extract-and-Expand Key Derivation Function (HKDF) for Rust.

- [MACs](https://github.com/RustCrypto/MACs) Collection of Message
 Authentication Code algorithms written in pure Rust including CMAC, HMAC, and
 PMAC.

- [Poseidon252](https://github.com/dusk-network/poseidon252) Reference
 implementation for the Poseidon Hashing algorithm.

- [RIPEMD160](https://github.com/RustCrypto/hashes/tree/master/ripemd160)
 Pure Rust implementation of the RIPEMD160 hash function.

- [SHA-2](https://github.com/RustCrypto/hashes/tree/master/sha2) Pure Rust
 implementation of the SHA-2 hash function family including SHA-224, SHA-256,
 SHA-384, and SHA-512.

- [SHA-3](https://github.com/RustCrypto/hashes/tree/master/sha3) Pure Rust
 implementation of the SHA-3 (Keccak) hash function.

- [universal-hashes](https://github.com/RustCrypto/universal-hashes)
 [![][audited-badge]](https://research.nccgroup.com/2020/02/26/public-report-rustcrypto-aes-gcm-and-chacha20poly1305-implementation-review/)
 Collection of Universal Hash Functions written in pure Rust including
 GHASH, POLYVAL, and Poly1305.

### Password Hashing Functions

- [argon2](https://github.com/RustCrypto/password-hashes/tree/master/argon2)
 Pure Rust implementation of the Argon2 password hashing function.

- [bcrypt](https://github.com/Keats/rust-bcrypt) Pure Rust implementation of
 the bcrypt password hashing function.

- [pbkdf2](https://github.com/RustCrypto/password-hashes/tree/master/pbkdf2)
 Pure Rust implementation of the Password-Based Key Derivation Function v2
 (PBKDF2).

- [phpass](https://github.com/clausehound/phpass)
  Pure Rust implementation of the PhPass algorithm used by WordPress.

- [pkcs5](https://github.com/RustCrypto/formats/tree/master/pkcs5)
 Pure Rust implementation of Public-Key Cryptography Standards #5: Password-Based
 Cryptography Specification Version 2.1 (RFC 8018) with support for the scrypt
 and PBKDF2 password-based key derivation functions.

- [rust-argon2](https://github.com/sru-systems/rust-argon2) Rust library for
 hashing passwords using Argon2, the password-hashing function that won the
 Password Hashing Competition (PHC).

- [scrypt](https://github.com/RustCrypto/password-hashes/tree/master/scrypt)
 Pure Rust implementation of the scrypt key derivation function.

## Asymmetric Cryptography

[up](#table-of-contents)

These crates implement individual asymmetric (a.k.a. public key) cryptography
algorithms.

### Asymmetric Primitives

- [ark-curves](https://github.com/arkworks-rs/curves) Implementation of a
 number of popular elliptic curves.

- [curve25519-dalek](https://github.com/dalek-cryptography/curve25519-dalek)
 [![][audited-badge]](https://blog.quarkslab.com/security-audit-of-dalek-libraries.html)
 A pure-Rust implementation of group operations on the
 [Ristretto](https://ristretto.group) and Curve25519 elliptic curves.

- [bls12_381](https://github.com/zkcrypto/bls12_381) Implementation of the
 BLS12-381 pairing-friendly elliptic curve group.

- [bn](https://github.com/paritytech/bn) Pairing cryptography library written
 in pure Rust, making use of the Barreto-Naehrig (BN) curve construction.

- [bp256](https://github.com/RustCrypto/elliptic-curves/tree/master/bp256)
 Brainpool P-256 elliptic curves.

- [fiat-rust](https://github.com/mit-plv/fiat-crypto/tree/master/fiat-rust)
 ![][verified-badge] Formally verified arithmetic implementations for several
 elliptic curves and word sizes, extracted to Rust from specifications
 written using in the Coq theorem prover.

- [h2c-rust-ref](https://github.com/armfazh/h2c-rust-ref)
 Pure Rust reference implementation of the hash to curve specification from
 IETF/CFRG Hash to Curve
 [document](https://datatracker.ietf.org/doc/draft-irtf-cfrg-hash-to-curve).
 Contains hashing methods for elliptic curves in Weierstrass, Montgomery,
 and Twisted Edwards form.

- [jubjub](https://github.com/zkcrypto/jubjub) Pure Rust implementation of
 the Jubjub elliptic curve group and its associated fields.

- [k256](https://github.com/RustCrypto/elliptic-curves/tree/master/k256) Pure
 Rust implementation of the secp256k1 (K-256) elliptic curve using complete
 formulas based on projective coordinates.

- [libsecp256k1-rs](https://github.com/sorpaas/libsecp256k1-rs) Pure Rust
 implementation of secp256k1.

- [p256](https://github.com/RustCrypto/elliptic-curves/tree/master/p256) Pure
 Rust implementation of the NIST P-256 elliptic curve (a.k.a. prime256v1,
 secp256r1).

- [pasta_curves](https://github.com/zcash/pasta_curves/)
 Rust implementation of the Pallas-Vesta curve cycle for recursive
 zero-knowledge proofs.

- [RSA](https://github.com/RustCrypto/RSA)
 [![][audited-badge]](https://delta.chat/assets/1907-otf-deltachat-rpgp-rustrsa-gb-reportv1.pdf)
 Pure Rust implementation of the RSA algorithm.

- [redox-ecc](https://github.com/armfazh/redox-ecc)
 Pure Rust reference implementation of the elliptic curve operations for
 Weierstrass, Montgomery, and Twisted Edwards curves.

- [rust-secp256k1](https://github.com/rust-bitcoin/rust-secp256k1) Rust FFI
 bindings for Bitcoin Core's secp256k1 library written in C.

### Digital Signatures

- [bls_like](https://github.com/w3f/bls) Aggregate BLS signatures with
 extensive tuning options.

- [bls-signatures](https://github.com/filecoin-project/bls-signatures)
 Implementation of BLS Signatures in pure Rust.

- [ecdsa](https://github.com/RustCrypto/signatures/tree/master/ecdsa) Pure
 Rust implementation of the Elliptic Curve Digital Signature Algorithm (ECDSA)
 as specified in FIPS 186-4 (Digital Signature Standard).

- [ed25519](https://github.com/RustCrypto/signatures/tree/master/ed25519)
 Cross-library compatibility crate for Edwards Digital Signature Algorithm
 (EdDSA) over Curve25519 as specified in RFC 8032.

- [ed25519-dalek](https://github.com/dalek-cryptography/ed25519-dalek)
 [![][audited-badge]](https://blog.quarkslab.com/security-audit-of-dalek-libraries.html)
 Fast and efficient ed25519 key generation, signing, and verification in
 Rust.

- [ed25519-zebra](https://github.com/ZcashFoundation/ed25519-zebra)
 Zcash-flavored Ed25519 signatures for consensus-critical applications.

- [milagro_bls](https://github.com/sigp/milagro_bls) BLS signatures using the
 [Apache Milagro](https://github.com/apache/incubator-milagro-crypto-rust)
 Cryptographic Library.

- [nisty](https://github.com/nickray/nisty) NIST P-256 signatures for
 Cortex-M4 microcontrollers.

- [rust-minisign](https://github.com/jedisct1/rust-minisign/) Pure Rust
 implementation of the [Minisign](https://jedisct1.github.io/minisign/)
 signature system.

- [schnorrkel](https://github.com/w3f/schnorrkel) Implements Schnorr
 signature on Ristretto compressed Ed25519 points, as well as related
 protocols like HDKD, MuSig, and a verifiable random function (VRF).

### Encryption (Hybrid Encryption)

- [hpke-rs](https://github.com/franziskuskiefer/hpke-rs) - Implementation of
 [HPKE](https://cfrg.github.io/draft-irtf-cfrg-hpke/draft-irtf-cfrg-hpke.html)
 using
 [Evercrypt](https://github.com/franziskuskiefer/evercrypt-rust/tree/master/evercrypt-rs).

- [rust-hpke](https://github.com/rozbb/rust-hpke) Early implementation of the
 [HPKE](https://datatracker.ietf.org/doc/draft-irtf-cfrg-hpke/) hybrid
 encryption standard, written in pure Rust.

### Key Exchange

- [opaque-ke](https://github.com/novifinancial/opaque-ke) A Rust
 implementation of the [OPAQUE](https://eprint.iacr.org/2018/163.pdf)
 Password-Authenticated Key Exchange protocol.

- [PAKEs](https://github.com/RustCrypto/PAKEs) Collection of
 Password-Authenticated Key Agreement protocols.

- [x25519-dalek](https://github.com/dalek-cryptography/x25519-dalek)
 [![][audited-badge]](https://blog.quarkslab.com/security-audit-of-dalek-libraries.html)
 Pure-Rust implementation of x25519 elliptic curve Diffie-Hellman key
 exchange, with curve operations provided by
 [curve25519-dalek](https://github.com/dalek-cryptography/curve25519-dalek).

### Threshold & Multiparty Signatures

- [multi-party-ecdsa](https://github.com/KZen-networks/multi-party-ecdsa)
 Rust implementation of {t,n}-threshold ECDSA (elliptic curve digital
 signature algorithm).

- [multi-party-schnorr](https://github.com/KZen-networks/multi-party-schnorr)
 Multiparty and threshold Schnorr signatures

- [threshold_crypto](https://github.com/poanetwork/threshold_crypto) A
 pairing-based threshold cryptosystem for collaborative decryption and
 signatures.

- [FROST (on redjubjub)](https://github.com/ZcashFoundation/redjubjub)
 [![][audited-badge]](https://github.com/ZcashFoundation/redjubjub/blob/main/zcash-frost-audit-report-20210323.pdf)
 An implementation of FROST (Flexible Round-Optimized Schnorr Threshold)
 RedJubjub signatures.

### Verifiable Delay Functions (VDFs)

- [vdf](https://github.com/poanetwork/vdf) An implementation of Verifiable
 Delay Functions in Rust.

### Verifiable Random Functions (VRFs)

- [schnorrkel](https://github.com/w3f/schnorrkel) Implements Schnorr
 signature on Ristretto compressed Ed25519 points, as well as related
 protocols like HDKD, MuSig, and a verifiable random function (VRF).

## Platform / Framework Bindings

[up](#table-of-contents)

These libraries are FFI bindings to OS platforms and commonly used
cryptography frameworks.

- [mesalink](https://mesalink.io/) OpenSSL-compatible C library implemented in
 Rust

- [native-tls](https://github.com/sfackler/rust-native-tls) An abstraction
 over platform-specific TLS implementations.

- [openssl](https://github.com/sfackler/rust-openssl) OpenSSL FFI bindings
 for the Rust programming language.

- [schannel](https://github.com/steffengy/schannel-rs) Rust bindings to the
 Windows SChannel APIs providing TLS client and server functionality.

- [security-framework](https://github.com/kornelski/rust-security-framework)
 Bindings to the Apple's Security.framework. Allows use of TLS and Keychain
 from Rust.

## Cryptographic Hardware

[up](#table-of-contents)

These libraries provide host-side drivers for cryptographic hardware devices
(e.g. authentication tokens, HSMs).

- [cryptoki](https://github.com/parallaxsecond/rust-cryptoki) Rust-native
 PKCS#11 library.

- [pkcs11](https://github.com/mheese/rust-pkcs11) Rust PKCS#11 Library.

- [rust-cryptoauthlib](https://github.com/PelionIoT/rust-cryptoauthlib/)
 Rust library for interfacing with ATECCx08a devices.

- [solo](https://github.com/solokeys/solo) Solo is an open source security
 key.

- [tss-esapi](https://github.com/parallaxsecond/rust-tss-esapi) Rust-native
 library for interfacing with TPM 2.0 devices via the TCG Enhanced System API
 (ESAPI).

- [yubihsm](https://github.com/iqlusioninc/yubihsm.rs) Pure-Rust client
 library for YubiHSM 2 devices which implements most the functionality of the
 libyubihsm C library from Yubico's YubiHSM SDK.

- [yubikey](https://github.com/iqlusioninc/yubikey.rs) Pure Rust
 cross-platform host-side driver for YubiKey devices from Yubico with support
 for public-key encryption and digital signatures using the Personal Identity
 Verification (PIV) application.

## Post-Quantum Cryptography

[up](#table-of-contents)

These libraries are designed to be secure against hypothetical future attacks
by large quantum computers.

- [oqs](https://github.com/open-quantum-safe/liboqs-rust) Wrapper around
 Open-Quantum-Safe's liboqs cryptographic library.

- [pqcrypto](https://github.com/rustpq/pqcrypto) FFI bindings to quantum-safe
 cryptographic libraries.

- [picnic-bindings](https://github.com/ait-crypto/picnic-bindings-rs) FFI
  bindings to Picnic library implementating the traits from
  [signature](https://github.com/RustCrypto/traits/tree/master/signature).

- [pqcrypto-picnic](https://github.com/ait-crypto/pqcrypto-picnic) FFI bindings
  to Picnic library implementating the traits from
  [pqcrypto](https://github.com/rustpq/pqcrypto).

## Random Number Generators

[up](#table-of-contents)

- [rand](https://github.com/rust-random/rand) Rust library for random number
 generation.

- [getrandom](https://docs.rs/getrandom/0.2.3/getrandom/) Interface to the
 operating system's random number generator.

## Zero-knowledge Proofs

[up](#table-of-contents)

- [arkworks](https://github.com/arkworks-rs) An ecosystem for developing and
 programming with zkSNARKs.

- [bellman](https://github.com/zkcrypto/bellman)
 [![](https://img.shields.io/badge/1-audited-success.svg)](https://cybermashup.files.wordpress.com/2018/08/zcash-audit.pdf)
 [![](https://img.shields.io/badge/2-audited-success.svg)](https://raw.githubusercontent.com/QED-it/sapling-audit/master/sapling-audit-report.pdf)
 A crate for building zk-SNARK circuits.

- [bellman-ce](https://github.com/matter-labs/bellman) Bellman fork with
 support for Ethereum's BN256.

- [bellperson](https://github.com/filecoin-project/bellperson) Bellman fork
 with GPU parallel acceleration for FFT and Multiexponentation subroutines in
 the Groth16 prover.

- [bulletproofs](https://github.com/dalek-cryptography/bulletproofs)
 [![][audited-badge]](https://blog.quarkslab.com/security-audit-of-dalek-libraries.html)
 Pure-Rust implementation of
 [Bulletproofs](https://crypto.stanford.edu/bulletproofs/) using
 [Ristretto](https://ristretto.group).

- [bulletproof](https://github.com/KZen-networks/bulletproofs) Implements
 [Bulletproofs+](https://eprint.iacr.org/2020/735.pdf) and
 [Bulletproofs](https://eprint.iacr.org/2017/1066.pdf) aggregated range proofs
 with multi-exponent verification.

- [Dusk-Zerocaf](https://github.com/dusk-network/dusk-zerocaf) Pure-Rust
 cryptographic library constructed to define operations for an elliptic curve
 embedded into the [Ristretto](https://ristretto.group) scalar field.

- [merlin](https://github.com/dalek-cryptography/merlin) Composable proof
 transcripts for public-coin arguments of knowledge.

- [OpenZKP](https://github.com/0xProject/OpenZKP) Pure-Rust implementations
 of Zero-Knowledge Proof systems.

- [snarkVM](https://github.com/AleoHQ/snarkVM) A Rust implementation of
 [Zexe](https://eprint.iacr.org/2018/962.pdf), a model for decentralized private
 computation using zero-knowledge proofs

- [Spartan](https://github.com/microsoft/Spartan) High-speed zkSNARKs without
 trusted setup.

- [winterfell](https://github.com/novifinancial/winterfell/) A distributed
 STARK prover.

- [ZoKrates](https://github.com/Zokrates/ZoKrates) A toolbox for zkSNARKs on
 Ethereum.

- [zkp](https://github.com/zkcrypto/zkp) Macro-based zero-knowledge proof
 compiler for Schnorr proofs.

## Secure Multiparty Computation

[up](#table-of-contents)

These libraries allow several participants to collectively perform a
computation without revealing what is being computed to the participants.

- [libpaillier](https://github.com/mikelodder7/paillier-rs) Rust
 implementation of the Paillier cryptosystem with additive homomorphism

- [swanky](https://github.com/GaloisInc/swanky) A suite of Rust libraries for
 secure multi-party computation.

- [white-city](https://github.com/KZen-networks/white-city) API to integrate
 distributed network for secure computation protocols.

## Fully Homomorphic Encryption

[up](#table-of-contents)

These libraries allow to perform secure computation, e.g. computations over
encrypted data.

- [concrete](https://github.com/zama-ai/concrete) Rust implementation of
 various FHE operations based on the TFHE scheme.

## Format Decoders/Encoders

[up](#table-of-contents)

These libraries implement parsers and serializers for various
cryptography-related formats.

- [base64ct](https://github.com/RustCrypto/formats/tree/master/base64ct)
 Constant-time Base64 decoder/encoder with `no_std` support.

- [der](https://github.com/RustCrypto/formats/tree/master/der)
 Cryptography-oriented ASN.1 DER decoder/encoder with `no_std` support.

- [pem-rfc7468](https://github.com/RustCrypto/formats/tree/master/pem-rfc7468)
 Constant-time implementation of the strict PEM encoding rules for PKIX, PKCS,
 and CMS Structures.

- [pkcs1](https://github.com/RustCrypto/formats/tree/master/pkcs1) Pure Rust
 implementation of Public-Key Cryptography Standards #1: RSA Cryptography
 Specifications Version 2.2 (RFC 8017).

- [pkcs8](https://github.com/RustCrypto/formats/tree/master/pkcs8) Pure Rust
 implementation of Public-Key Cryptography Standards #8: Private-Key
 Information Syntax Specification (RFC 5208).

- [rasn](https://github.com/XAMPPRocky/rasn) A `no_std` ASN.1 codec framework
 (like serde but for ASN.1). Supports the following formats: BER, CER, DER.

- [x509-parser](https://github.com/rusticata/x509-parser) X.509 v3 (RFC5280)
 parser, implemented with the nom parser combinator framework.

## Defensive Measures

[up](#table-of-contents)

These libraries can be used to harden cryptographic algorithms against
attacks.

### Constant-Time Code

- [subtle](https://github.com/dalek-cryptography/subtle)
 [![][audited-badge]](https://blog.quarkslab.com/security-audit-of-dalek-libraries.html)
 Pure-Rust traits and utilities for constant-time cryptographic implementations.

### Protecting Secrets in Memory

- [secrecy](https://github.com/iqlusioninc/crates/tree/main/secrecy) A simple
 secret-keeping library for Rust.

### Zeroing Memory

- [zeroize](https://github.com/RustCrypto/utils/tree/master/zeroize) Securely
 zero memory while avoiding compiler optimizations.

## Arithmetic

[up](#table-of-contents)

These libraries implement mathematical algorithms potentially interesting for
cryptography-related applications.

- [crypto-bigint](https://github.com/RustCrypto/crypto-bigint)
 Cryptography-oriented "bignum" library with constant-time algorithms
 including modular arithmetic, stack-allocated big integers, and `no_std`
 support

- [nalgebra](https://github.com/rustsim/nalgebra) Linear algebra library for
 Rust.

- [num](https://github.com/rust-num/num) Collection of numeric types and
 traits for Rust. (Bigint).

- [rust-decimal](https://github.com/paupino/rust-decimal) Decimal
 implementation written in pure Rust suitable for financial calculations that
 require significant integral and fractional digits with no round-off errors.

- [secret-integers](https://github.com/hacspec/rust-secret-integers)
  Integer wrapper types that guarantee constant-time operations only.

## Miscellany

[up](#table-of-contents)

Other libraries which don't fall into the categories listed above.

- [librustzcash](https://github.com/zcash/librustzcash) A (work-in-progress)
 set of Rust crates for working with Zcash.

- [sequoia](https://gitlab.com/sequoia-pgp/sequoia) Implements OpenPGP in
 Rust.
