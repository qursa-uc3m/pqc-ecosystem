# PQC Libraries & TLS/DTLS PQC Support Overview

This repository collects data on Post-Quantum Cryptography (PQC) libraries, wrappers, and TLS/DTLS libraries that have PQC support. The tables show details like the algorithms used, programming languages, bindings, recent commits, and more. Contributions are welcome if you see updates or missing entries.

## PQC Libraries & Wrappers

### PQC Libraries

| Library    | Algorithms        | Language    | Bindings                          | Commits | Last Update  | Stars |
|------------|-------------------|-------------|-----------------------------------|---------|--------------|-------|
| [PQClean](https://github.com/PQClean/PQClean)    | NIST and others   | C/Assembly  | -                                 | 1387    | 2 days ago   | 637   |
| [liboqs](https://github.com/open-quantum-safe/liboqs)     | NIST and others   | C/Assembly  | C++, Python, Go, Rust, Java         | 1554    | Last week    | 2100  |
| [wolfCrypt](https://github.com/wolfSSL/wolfssl)  | NIST              | C/Assembly  | ADA, Rust, Python, Node.js         | 24555   | Yesterday    | 2400  |
| [CIRCL](https://github.com/cloudflare/circl)     | NIST and others   | Go          | -                                 | 646     | Last month   | 1400  |

### Wrapper Libraries

| Wrapper Library | Integrates | Bindings                          | Commits | Last Update   | Stars |
|-----------------|------------|-----------------------------------|---------|---------------|-------|
| [liboqs](https://github.com/open-quantum-safe/liboqs)          | PQClean    | C, C++, Python, Go, Rust, Java    | 1554    | Last week     | 2100  |
| [pqm4](https://github.com/mupq/pqm4)           | PQClean    | C (targeting ARM Cortex-M4)       | 416     | Last week     | 318   |
| [pqcrypto](https://github.com/rustpq/pqcrypto)        | PQClean    | Rust                              | 241     | 2 weeks ago   | 271   |
| [node-pqclean](https://github.com/tniessen/node-pqclean)    | PQClean    | Node.js                           | 120     | 2 months ago  | 75    |
| [quantcrypt](https://github.com/aabmets/quantcrypt)      | PQClean    | Python                            | 175     | Last year     | 37    |

## TLS/DTLS Libraries with PQC Support

| Library                 | Protocols                                        | Algorithms                          | Integrates | Language        |
|-------------------------|--------------------------------------------------|-------------------------------------|------------|-----------------|
| [OpenSSL](https://github.com/openssl/openssl)                 | TLS 1.3 (oqs-provider), DTLS 1.3 soon            | All NIST and more                   | liboqs     | C               |
| [Bouncy Castle](https://github.com/bcgit/bc-java)          | TLS 1.3                                          | All NIST                            | -          | Java, C#, Kotlin|
| [wolfSSL]((https://github.com/wolfSSL/wolfssl))                 | TLS 1.3, DTLS 1.3                                | All NIST                            | liboqs     | C               |
| [Rustls](https://github.com/rustls/rustls)                  | TLS 1.3 [(rustls-post-quantum](https://crates.io/crates/rustls-post-quantum))                    | MLKEM768, X25519MLKEM768             | -          | Rust            |
| [Mbed TLS](https://github.com/Mbed-TLS/mbedtls)                | TLS 1.3                                          | All NIST                            | liboqs     | C               |
| [Botan](https://github.com/randombit/botan)                   | TLS 1.3                                          | All NIST and more                   | -          | C++             |
| [S2n-tls](https://github.com/aws/s2n-tls)           | TLS 1.3                                          | Kyber                               | -          | C               |
| [NSS](https://github.com/nss-dev/nss)           | TLS 1.3                                          | mlkem768x25519                      | -          | C/C++           |
| [BoringSSL](https://boringssl.googlesource.com/boringssl)      | TLS 1.3 (+ OQS and Cloudflare forks)             | All NIST                            | -          | C               |
| [Fizz](https://github.com/facebookincubator/fizz)             | TLS 1.3                                          | All NIST and more                   | liboqs     | C++             |
| [SymCrypt](https://github.com/microsoft/SymCrypt)    | TLS 1.3                                          | All NIST                            | -          | C               |

## Protocol Integrations

This section lists quantum-safe protocol demos that use liboqs and related tools. For more details, see the [oqs-demos repository](https://github.com/open-quantum-safe/oqs-demos).

## IPSec

| Project                | Description                                                                                  | GitHub Repo                                                             | Via                | Transport | Version                                | Status       |
|------------------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------|-----------|----------------------------------------|--------------|
| strongSwan   | IPSec solution with quantum-safe integration via liboqs (using the oqs plugin)                | [strongswan/strongswan](https://github.com/strongswan/strongswan)        | liboqs/oqs-provider | IPSec     | strongswan-6.0.0beta4 / liboqs-0.8.0     | Experimental |

## HTTPS

| Project      | Description                                         | GitHub Repo                                                                                          | Via                | Transport | Status       |
|--------------|-----------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------|-----------|--------------|
| curl         | HTTPS client with quantum-safe TLS support          | [oqs-demos/curl](https://github.com/open-quantum-safe/oqs-demos/tree/main/curl)                       | liboqs/oqs-provider | TLS 1.3   | Maintained   |
| Apache httpd | HTTPS server with quantum-safe TLS support          | [oqs-demos/httpd](https://github.com/open-quantum-safe/oqs-demos/tree/main/httpd)                     | liboqs/oqs-provider | TLS 1.3   | Maintained   |
| nginx        | HTTPS server with experimental quantum-safe support | [oqs-demos/nginx](https://github.com/open-quantum-safe/oqs-demos/tree/main/nginx)                     | liboqs/oqs-provider | TLS 1.3   | Maintained   |
| Chromium     | Browser demo for quantum-safe TLS interoperability    | [oqs-demos/chromium](https://github.com/open-quantum-safe/oqs-demos/tree/main/chromium)               | liboqs/oqs-provider | TLS 1.3   | Experimental |

## SSH

| Project  | Description                                          | GitHub Repo                                                                                         | Via                | Transport | Status       |
|----------|------------------------------------------------------|-----------------------------------------------------------------------------------------------------|--------------------|-----------|--------------|
| OpenSSH  | SSH integration demo with quantum-safe support       | [oqs-demos/openssh](https://github.com/open-quantum-safe/oqs-demos/tree/main/openssh)                 | liboqs/oqs-provider | SSH       | Maintained |

## CoAP

| Project | Description                                                      | GitHub Repo                                   | Via     | Transport | Status       |
|---------|------------------------------------------------------------------|-----------------------------------------------|---------|-----------|--------------|
| libcoap | CoAP protocol with quantum-safe DTLS transport integration       | [libcoap](https://github.com/obgm/libcoap)    | wolfSSL | DTLS      | Mantained |

## MQTT

| Project   | Description                                                                                         | GitHub Repo                                                                                                 | Via                | Transport     | Version                                          | Status       |
|-----------|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|--------------------|---------------|--------------------------------------------------|--------------|
| Mosquitto | MQTT broker with quantum-safe TLS support using OpenSSL v3 and the OQS provider integration         | [oqs-demos/mosquitto](https://github.com/open-quantum-safe/oqs-demos/tree/main/mosquitto)                      | liboqs/oqs-provider | MQTT over TLS | Mosquitto v2.0.20 / OpenSSL v3, liboqs integration | Maintained   |

## MQTT-SN

| Project                                  | Description                                                       | GitHub Repo                                                                                                  | Via      | Transport      | Status       |
|------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|----------|----------------|--------------|
| paho.mqtt-sn.embedded-c.wolfssl-pq         | MQTT-SN integration with quantum-safe support via wolfSSL         | [paho.mqtt-sn.embedded-c.wolfssl-pq](https://github.com/qursa-uc3m/paho.mqtt-sn.embedded-c.wolfssl-pq)          | wolfSSL  | DTLS | Experimental |
| wolfMQTT                                 | MQTT client with built-in quantum-safe support (via wolfSSL)         | [wolfMQTT](https://www.wolfssl.com/wolfmqtt/)                                     | wolfSSL  | DTLS     | Maintained   |

## DDS

| Project            | Description                                                          | GitHub Repo                                                       | Via                | Transport | Status       |
|--------------------|----------------------------------------------------------------------|-------------------------------------------------------------------|--------------------|-----------|--------------|
| CycloneDDS Plugin  | DDS integration with quantum-safe support via a CycloneDDS plugin     | [pqsec-dds](https://github.com/qursa-uc3m/pqsec-dds)                | liboqs/oqs-provider | UDP, TCP, shared memory       | Experimental |

## Zenoh

| Project | Description                                                | GitHub Repo                                          | Via                  | Transport | Status       |
|---------|------------------------------------------------------------|------------------------------------------------------|----------------------|-----------|--------------|
| Zenoh   | Zenoh protocol integration with quantum-safe support       | [Zenoh Fork](https://github.com/fj-blanco/zenoh)     | rustls-post-quantum  | Zenoh     | Experimental |

## How to Contribute

- **Report Issues:** If you find errors or outdated info, please open an issue.
- **Submit Updates:** Feel free to create pull requests to add new libraries or update existing entries.
- **Data Sources:** Ensure your contributions come with verifiable sources or links.

## License

This repository is licensed under the [MIT License](LICENSE).