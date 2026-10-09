# Open-source license bundle

This PCKB 0.7.0 macOS arm64 package retains verified historical component notices and adds exact locked upstream license texts for current macOS attribution. `LICENSE_INDEX.tsv` maps each component to complete license, copyright, and notice evidence by SHA-256. License texts are preserved byte-for-byte. Historical Windows notices are retained for reference only; no Windows 0.7.0 binary is distributed.

`../MACOS_COMPONENT_INVENTORY.tsv` identifies current final-link Rust components, production frontend packages, and conservative inline/macro attribution for Unicode-normalization transitive dependencies. It does not confuse inline dependencies with separate loaded archives. Toolchain/runtime, AWS-LC, SQLite, and their existing full composite notices are retained. The objc2 SDK-derived-work uncertainty notice is retained unchanged and is not represented as a new legal resolution.

Final-link evidence is retained privately; current package/version attribution is recorded in `../MACOS_COMPONENT_INVENTORY.tsv`. License evidence SHA-256 values remain in `LICENSE_INDEX.tsv`.
