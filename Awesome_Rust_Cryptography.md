# High-level Libraries

[rage](https://github.com/str4d/rage) Implementation of [age](https://age-encryption.org/)—a simple, secure and modern encryption tool with small explicit keys, no config options, and UNIX-style composability.

[sodiumoxide](https://github.com/sodiumoxide/sodiumoxide) Type-safe efficient Rust bindings to [libsodium](https://libsodium.org)

[snow](https://github.com/mcginty/snow) Implementation of Trevor Perrin's [Noise Protocol](https://noiseprotocol.org) that is designed to be Hard To Fuck Up™.

[strobe-rs](https://github.com/rozbb/strobe-rs) Relatively barebones, `no_std` implementation of the [Strobe protocol framework](https://strobe.sourceforge.io/) in pure Rust.


# Collections of Cryptographic Primitives

[evercrypt-rust](https://github.com/franziskuskiefer/evercrypt-rust) Rust bindings for [evercrypt](https://github.com/project-everest/hacl-star/tree/master/providers/evercrypt), a set of high-performance HACL\*-verified implementations of cryptographic primitives. bindings crate, bringing HACL-verified cryptographic primitives.

[libsm](https://github.com/citahub/libsm) China's Standards of Encryption Algorithms (SM2/3/4).

[orion](https://github.com/brycx/orion) Collection of usable, easy and safe pure-Rust cryptographic primitives.

[ring](https://github.com/briansmith/ring) Collection of cryptographic primitives, written in pure Rust. _ring_ is focused on the implementation, testing, and optimization of a core set of cryptographic operations exposed via an easy-to-use (and hard-to-misuse) API.

[rustls](https://github.com/ctz/rustls) Modern TLS library in Rust.


# Symmetric Cryptography

## Encryption

[aeads](https://github.com/RustCrypto/AEADs) Collection of Authenticated Encryption with Associated Data Algorithms: high-level encryption ciphers

[block-ciphers](https://github.com/RustCrypto/block-ciphers) Collection of block ciphers and block modes written in pure Rust.

[stream-ciphers](https://github.com/RustCrypto/stream-ciphers) Collection of stream cipher algorithms written in pure Rust.

## Hash Functions and Friends

[BLAKE3](https://github.com/BLAKE3-team/BLAKE3) Official implementation of the BLAKE3 cryptographic hash function.

[hashes](https://github.com/RustCrypto/hashes) Collection of cryptographic hash functions written in pure Rust.

[KDFs](https://github.com/RustCrypto/KDFs) Collection of Key Derivation Functions written in pure Rust.

[MACs](https://github.com/RustCrypto/MACs) Collection of Message Authentication Code algorithms written in pure Rust.

[password-hashes](https://github.com/RustCrypto/password-hashes) Collection of password hashing algorithms, otherwise known as password-based key derivation functions.

[Poseidon252](https://github.com/dusk-network/poseidon252) Reference implementation for the Poseidon Hashing algorithm.


# Asymmetric Cryptography

## Encryption (Hybrid Encryption)

[hpke-rs](https://github.com/franziskuskiefer/hpke-rs) - Implementation of [HPKE](https://cfrg.github.io/draft-irtf-cfrg-hpke/draft-irtf-cfrg-hpke.html) using [Evercrypt](https://github.com/franziskuskiefer/evercrypt-rust/tree/master/evercrypt-rs).

[rust-hpke](https://github.com/rozbb/rust-hpke) Early implementation of the [HPKE](https://datatracker.ietf.org/doc/draft-irtf-cfrg-hpke/) hybrid encryption standard, written in pure Rust.


## Key Exchange

[x25519-dalek](https://github.com/dalek-cryptography/x25519-dalek) A pure-Rust implementation of x25519 elliptic curve Diffie-Hellman key exchange, with curve operations provided by [curve25519-dalek](https://github.com/dalek-cryptography/curve25519-dalek).

[opaque-ke](https://github.com/novifinancial/opaque-ke) A Rust implementation of the [OPAQUE](https://eprint.iacr.org/2018/163.pdf) Password-Authenticated Key Exchange protocol.

[PAKEs](https://github.com/RustCrypto/PAKEs) Collection of Password-Authenticated Key Agreement protocols.


## Digital Signatures

[bls_like](https://github.com/w3f/bls) Aggregate BLS signatures with extensive tuning options.

[bls-signatures](https://github.com/filecoin-project/bls-signatures) Implementation of BLS Signatures in pure Rust.

[ed25519-dalek](https://github.com/dalek-cryptography/ed25519-dalek) Fast and efficient ed25519 key generation, signing, and verification in Rust.

[milagro_bls](https://github.com/sigp/milagro_bls) BLS signatures using the [Apache Milagro](https://github.com/apache/incubator-milagro-crypto-rust) Cryptographic Library.

[nisty](https://github.com/nickray/nisty) NIST P-256 signatures for Cortex-M4 microcontrollers.

[rust-minisign](https://github.com/jedisct1/rust-minisign/) Pure Rust implementation of the [Minisign](https://jedisct1.github.io/minisign/) signature system.

[schnorrkel](https://github.com/w3f/schnorrkel) Implements Schnorr signature on Ristretto compressed Ed25519 points, as well as related protocols like HDKD, MuSig, and a verifiable random function (VRF).

[signatures](https://github.com/RustCrypto/signatures) Collection of digital signature algorithms.

## Threshold & Multiparty Signatures

[multi-party-ecdsa](https://github.com/KZen-networks/multi-party-ecdsa) Rust implementation of {t,n}-threshold ECDSA (elliptic curve digital signature algorithm).

[multi-party-schnorr](https://github.com/KZen-networks/multi-party-schnorr) Multiparty and threshold Schnorr signatures

[threshold_crypto](https://github.com/poanetwork/threshold_crypto) A pairing-based threshold cryptosystem for collaborative decryption and signatures.

## Verifiable Delay Functions 

[vdf](https://github.com/poanetwork/vdf) An implementation of Verifiable Delay Functions in Rust.

## Verifiable Random Functions

[schnorrkel](https://github.com/w3f/schnorrkel) Implements Schnorr signature on Ristretto compressed Ed25519 points, as well as related protocols like HDKD, MuSig, and a verifiable random function (VRF).

## Asymmetric Primitives

[curve25519-dalek](https://github.com/dalek-cryptography/curve25519-dalek) A pure-Rust implementation of group operations on the [Ristretto](https://ristretto.group) and Curve25519 elliptic curves.

[BLS12-381](https://github.com/zkcrypto/bls12_381) Implementation of the BLS12-381 pairing-friendly elliptic curve group.

[bn](https://github.com/paritytech/bn) Pairing cryptography library written in pure Rust, making use of the Barreto-Naehrig (BN) curve construction.

[elliptic-curves](https://github.com/RustCrypto/elliptic-curves) General purpose Elliptic Curve Cryptography (ECC) support, including types and traits for representing various elliptic curve forms, scalars, points, and public/secret keys composed thereof.

[fiat-crypto](https://github.com/mit-plv/fiat-crypto) Formally verified arithmetic implementations for several elliptic curves and word sizes, extracted to Rust from specifications written using in the Coq theorem prover.

[Jubjub](https://github.com/zkcrypto/jubjub) Pure Rust implementation of the Jubjub elliptic curve group and its associated fields.

[libsecp256k1-rs](https://github.com/sorpaas/libsecp256k1-rs) Pure Rust Implementation of secp256k1.

[RSA](https://github.com/RustCrypto/RSA) An RSA implementation in pure Rust.

[rust-secp256k1](https://github.com/rust-bitcoin/rust-secp256k1) Rust bindings for Bitcoin secp256k1 library written in C.

# Random Number Generators

[rand](https://github.com/rust-random/rand) Rust library for random number generation.

# Zero-knowledge Proofs

[arkworks-rs](https://github.com/arkworks-rs) An ecosystem for developing and programming with zkSNARKs.

[bellman](https://github.com/zkcrypto/bellman) A crate for building zk-SNARK circuits.

[bellman-ce](https://github.com/matter-labs/bellman) Bellman fork with support for Ethereum's BN256.

[bellperson](https://github.com/filecoin-project/bellperson) Bellman fork with GPU parallel acceleration for FFT and Multiexponentation subroutines in the Groth16 prover.

[bulletproofs](https://github.com/dalek-cryptography/bulletproofs) Pure-Rust implementation of [Bulletproofs](https://crypto.stanford.edu/bulletproofs/) using [Ristretto](https://ristretto.group).

[bulletproof](https://github.com/KZen-networks/bulletproofs) Implements [Bulletproofs+](https://eprint.iacr.org/2020/735.pdf) and [Bulletproofs](https://eprint.iacr.org/2017/1066.pdf) aggregated range proofs with multi-exponent verification.

[Dusk-Zerocaf](https://github.com/dusk-network/dusk-zerocaf) Pure-Rust cryptographic library constructed to define operations for an elliptic curve embedded into the [Ristretto](https://ristretto.group) scalar field.

[merlin](https://github.com/dalek-cryptography/merlin) Composable proof transcripts for public-coin arguments of knowledge.

[OpenZKP](https://github.com/0xProject/OpenZKP) Pure-Rust implementations of Zero-Knowledge Proof systems.

[Spartan](https://github.com/microsoft/Spartan) High-speed zkSNARKs without trusted setup.

[ZoKrates](https://github.com/Zokrates/ZoKrates) A toolbox for zkSNARKs on Ethereum.


# Secure Multiparty Computation

[white-city](https://github.com/KZen-networks/white-city) API to integrate distributed network for secure computation protocols.


# Defensive Measures

## Constant time Code

[subtle](https://github.com/dalek-cryptography/subtle) Pure-Rust traits and utilities for constant-time cryptographic implementations.

## Zeroing memory

[zeroize](https://github.com/iqlusioninc/crates/tree/main/zeroize) Securely zero memory while avoiding compiler optimizations.


# Arithmetic

[nalgebra](https://github.com/rustsim/nalgebra) Linear algebra library for Rust.

[num](https://github.com/rust-num/num) Collection of numeric types and traits for Rust. (Bigint).

[rust-decimal](https://github.com/paupino/rust-decimal) A Decimal implementation written in pure Rust suitable for financial calculations that require significant integral and fractional digits with no round-off errors.


# Misc

[librustzcash](https://github.com/zcash/librustzcash) A (work-in-progress) set of Rust crates for working with Zcash.

[sequoia](https://gitlab.com/sequoia-pgp/sequoia) Implements OpenPGP in Rust.