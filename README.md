# PQC Libraries & TLS/DTLS PQC Support Overview

This repository collects data on Post-Quantum Cryptography (PQC) libraries, wrappers, and TLS/DTLS libraries that have PQC support. The tables show details like the algorithms used, programming languages, bindings, recent commits, and more. Contributions are welcome if you see updates or missing entries.

## Tables

### PQC Libraries & Wrappers

#### PQC Libraries

| Library    | Algorithms        | Language    | Bindings                          | Commits | Last Update  | Stars |
|------------|-------------------|-------------|-----------------------------------|---------|--------------|-------|
| [PQClean](https://github.com/PQClean/PQClean)    | NIST and others   | C/Assembly  | -                                 | 1387    | 2 days ago   | 637   |
| [liboqs](https://github.com/open-quantum-safe/liboqs)     | NIST and others   | C/Assembly  | C++, Python, Go, Rust, Java         | 1554    | Last week    | 2100  |
| [wolfCrypt](https://github.com/wolfSSL/wolfssl)  | NIST              | C/Assembly  | ADA, Rust, Python, Node.js         | 24555   | Yesterday    | 2400  |
| [CIRCL](https://github.com/cloudflare/circl)     | NIST and others   | Go          | -                                 | 646     | Last month   | 1400  |

#### Wrapper Libraries

| Wrapper Library | Integrates | Bindings                          | Commits | Last Update   | Stars |
|-----------------|------------|-----------------------------------|---------|---------------|-------|
| [liboqs](https://github.com/open-quantum-safe/liboqs)          | PQClean    | C, C++, Python, Go, Rust, Java    | 1554    | Last week     | 2100  |
| [pqm4](https://github.com/mupq/pqm4)           | PQClean    | C (targeting ARM Cortex-M4)       | 416     | Last week     | 318   |
| [pqcrypto](https://github.com/rustpq/pqcrypto)        | PQClean    | Rust                              | 241     | 2 weeks ago   | 271   |
| [node-pqclean](https://github.com/tniessen/node-pqclean)    | PQClean    | Node.js                           | 120     | 2 months ago  | 75    |
| [quantcrypt](https://github.com/aabmets/quantcrypt)      | PQClean    | Python                            | 175     | Last year     | 37    |

### TLS/DTLS Libraries with PQC Support

| Library                 | Protocols                                        | Algorithms                          | Integrates | Language        |
|-------------------------|--------------------------------------------------|-------------------------------------|------------|-----------------|
| [OpenSSL](https://github.com/openssl/openssl)                 | TLS 1.3 (oqs-provider), DTLS 1.3 soon            | All NIST and more                   | liboqs     | C               |
| [Bouncy Castle](https://github.com/bcgit/bc-java)          | TLS 1.3                                          | All NIST                            | -          | Java, C#, Kotlin|
| [wolfSSL]((https://github.com/wolfSSL/wolfssl))                 | TLS 1.3, DTLS 1.3                                | All NIST                            | liboqs     | C               |
| [Rustls](https://github.com/rustls/rustls)                  | TLS 1.3 (rustls_post_quantum)                    | MLKEM768, X25519MLKEM768             | -          | Rust            |
| [Mbed TLS](https://github.com/Mbed-TLS/mbedtls)                | TLS 1.3                                          | All NIST                            | liboqs     | C               |
| [Botan](https://github.com/randombit/botan)                   | TLS 1.3                                          | All NIST and more                   | -          | C++             |
| [S2n-tls](https://github.com/aws/s2n-tls)           | TLS 1.3                                          | Kyber                               | -          | C               |
| [NSS](https://github.com/nss-dev/nss)           | TLS 1.3                                          | mlkem768x25519                      | -          | C/C++           |
| [BoringSSL](https://boringssl.googlesource.com/boringssl)      | TLS 1.3 (+ OQS and Cloudflare forks)             | All NIST                            | -          | C               |
| [Fizz](https://github.com/facebookincubator/fizz)             | TLS 1.3                                          | All NIST and more                   | liboqs     | C++             |
| [SymCrypt](https://github.com/microsoft/SymCrypt)    | TLS 1.3                                          | All NIST                            | -          | C               |

## How to Contribute

- **Report Issues:** If you find errors or outdated info, please open an issue.
- **Submit Updates:** Feel free to create pull requests to add new libraries or update existing entries.
- **Data Sources:** Ensure your contributions come with verifiable sources or links.

## License

This repository is licensed under the [MIT License](LICENSE).