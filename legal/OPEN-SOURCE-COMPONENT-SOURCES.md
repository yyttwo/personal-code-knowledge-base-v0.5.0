# Open-source component sources

This document accompanies PCKB 0.7.1 Public Preview for macOS Apple Silicon (arm64).
PCKB first-party source code is proprietary and is not included.

The verified 0.3.0 binary audit found no MPL-covered component requiring
Source Code Form availability in the distributed artifact. The 0.4.0 delta
adds only the permissively licensed image-decoding components listed below;
it adds no GPL, AGPL, LGPL, MPL, or custom-license component.

| Component | Version | License | Exact upstream source |
| --- | --- | --- | --- |
| byteorder-lite | 0.1.0 | Unlicense OR MIT | https://github.com/image-rs/byteorder-lite/tree/7d44da06a48fe10d7e23efd9a932d18a7a2def63 |
| image | 0.25.10 | MIT OR Apache-2.0 | https://github.com/image-rs/image/tree/76e57184f22772dad1138e96954e57945406b15e |
| image-webp | 0.2.4 | MIT OR Apache-2.0 | https://github.com/image-rs/image-webp/tree/08b57d473c90148dd4b37a075df365afc3dfcc2b |
| moxcms | 0.8.1 | BSD-3-Clause OR Apache-2.0 | https://github.com/awxkee/moxcms/tree/c4affa196727d17f21a7f6f148a558867decb470 |
| pxfm | 0.1.30 | BSD-3-Clause OR Apache-2.0 | https://github.com/awxkee/pxfm/tree/acf7acd00cfc845307eda7b7b2de19e42303de82 |
| quick-error | 2.0.1 | MIT OR Apache-2.0 | https://github.com/tailhook/quick-error/tree/25ab982bb0c43130ae48485151f4a232eeab7d0c |
| zune-core | 0.5.3 | MIT OR Apache-2.0 OR Zlib | https://github.com/etemesi254/zune-image/tree/de5dfc800cfa063116eb695edb6ccd01cb96ea7a/crates/zune-core |
| zune-jpeg | 0.5.15 | MIT OR Apache-2.0 OR Zlib | https://github.com/etemesi254/zune-image/tree/31d81fed7551c8ccea456d9d8e2b1fd8bebb6995/crates/zune-jpeg |

Complete license texts and component-to-license mappings are in
`OPEN-SOURCE-LICENSES/`.

## Windows distribution delta for 0.6.0 Public Preview

This section supplements the verified macOS baseline. Private final map/PDB
contributions and the extracted payload are checked separately from Cargo's
dependency graph; installed legal resources must match this bundle byte for byte.
PCKB first-party source remains proprietary; only third-party upstream sources
are referenced here. Existing objc2 uncertainty is unchanged.

| Component | Version | License | Exact upstream source |
| --- | --- | --- | --- |
| NSIS engine, standard plugins and graphics | 3.11 | zlib/libpng | https://sourceforge.net/projects/nsis/files/NSIS%203/3.11/ |
| NSIS LZMA module | bundled with NSIS 3.11 | CPL-1.0 with LZMA linking exception | https://sourceforge.net/projects/nsis/files/NSIS%203/3.11/nsis-3.11-src.tar.bz2/download |
| nsis-tauri-utils | 0.5.3 | MIT OR Apache-2.0 | https://github.com/tauri-apps/nsis-tauri-utils/tree/13d9edd27b69310e108d6fbd49f90992f8a05390 |
| semver in nsis-tauri-utils | 1.0 series; exact resolved patch unpublished | MIT | https://github.com/dtolnay/semver |
| Tauri NSIS installer template | locked CLI 2.11.4 | MIT OR Apache-2.0 | https://github.com/tauri-apps/tauri/tree/8909f221d1515955fc843808032bdc5d62209c96/crates/tauri-bundler/src/bundle/windows/templates |
| Microsoft WebView2Loader | SDK 1.0.3650.58 | original Microsoft SDK redistribution terms | https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.3650.58 |
| bit-set | 0.8.0 | Apache-2.0 OR MIT | https://github.com/contain-rs/bit-set/tree/2b8861d23b53d63d326d2694ddabde6e7b19fbd0 |
| dpi | 0.1.2 | Apache-2.0 AND MIT | https://github.com/rust-windowing/winit/tree/587ade844dfb0eada3696ba1cb263c66eea80581 |
| fraction | 0.17.0 | MIT OR Apache-2.0 | https://github.com/dnsl48/fraction/tree/53d04cddb4640d1fe7756c289b3ce34be14da504 |
| futures-util | 0.3.34 | MIT OR Apache-2.0 | https://github.com/rust-lang/futures-rs/tree/705e6b5c0f06535b1aac1cb1989a172b3d45be8c |
| hashbrown | 0.17.1 | MIT OR Apache-2.0 | https://github.com/rust-lang/hashbrown/tree/c62a63a61b7caf2de8f9ecb7b06a66b0ab6bdf3d |
| micromap | 0.3.0 | MIT | https://github.com/yegor256/micromap/tree/72d6d2b26678b6e41d2bc94d215e619b94a4fa75 |
| num-rational | 0.4.2 | MIT OR Apache-2.0 | https://github.com/rust-num/num-rational/tree/4d55ad22ac86ebbc4cb45d79a956e4a1f7af57d1 |
| phf | 0.13.1 | MIT | https://github.com/rust-phf/rust-phf/tree/1e518a6e94a2444b8df7d89078cfc69859537971 |
| phf_shared | 0.13.1 | MIT | https://github.com/rust-phf/rust-phf/tree/1e518a6e94a2444b8df7d89078cfc69859537971 |
| smallvec | 1.16.0 | MIT OR Apache-2.0 | https://github.com/servo/rust-smallvec/tree/aa22a8ff83108228b6d941b83fc91399267d72c9 |
| softbuffer | 0.4.8 | MIT OR Apache-2.0 | https://github.com/rust-windowing/softbuffer/tree/d871852faa1137d4615b99b9ad31c3ba80f345b5 |
| tokio-rustls | 0.26.5 | MIT OR Apache-2.0 | https://github.com/rustls/tokio-rustls/tree/f8832d28ce5688f101368e34fc6b49899a8d4293 |
| unicode-general-category | 1.1.0 | Apache-2.0 | https://github.com/yeslogic/unicode-general-category/tree/cb2d8a62f035c33d6971b99322aae65f3cea7c88 |
| unicode-segmentation | 1.13.3 | MIT OR Apache-2.0 | https://github.com/unicode-rs/unicode-segmentation/tree/66a032fd8d667bc47ac5b640b151dff3f5356d07 |
| webview2-com | 0.38.2 | MIT | https://github.com/wravery/webview2-rs/tree/b74dc5e2b394044bea5191052868ce7a106c202c |
| windows-core | 0.61.2 | MIT OR Apache-2.0 | https://github.com/microsoft/windows-rs/tree/49e5d37ef31838d027c41ee28d696e046d04c27f |
| windows-strings | 0.4.2 | MIT OR Apache-2.0 | https://github.com/microsoft/windows-rs/tree/49e5d37ef31838d027c41ee28d696e046d04c27f |
| windows | 0.61.3 | MIT OR Apache-2.0 | https://github.com/microsoft/windows-rs/tree/4b8893b307719ec23cce698269ca572ef301dc5c |

Only LZMA compression was found in the candidate; no unused bzip2 or zlib
compression module is added to this delta. NSIS LZMA source-availability
obligations apply to that module, not to independent proprietary PCKB code.
The full WebView2 Runtime is obtained separately from Microsoft when needed;
it is not claimed to be embedded in the PCKB installer.

### Additional Windows source and inline provenance

Conservative notices also cover inline/source provenance from the private final
PDB, beyond standalone archive owners. Cargo's target graph alone is not used
as evidence of distribution.

| Component | Version | License | Exact upstream source |
| --- | --- | --- | --- |
| alloc-no-stdlib | 2.0.4 | BSD-3-Clause | https://github.com/dropbox/rust-alloc-no-stdlib/tree/6032b6a9b20e03737135c55a0270ccffcc1438ef |
| alloc-stdlib | 0.2.4 | BSD-3-Clause | https://github.com/dropbox/rust-alloc-no-stdlib/tree/ae42d22078b98549e987d2f03d12df7b984fde47 |
| allocator-api2 | 0.2.21 | MIT OR Apache-2.0 | https://github.com/zakarumych/allocator-api2/tree/63cd7fcc2f8854b5821c7054d026e8a4647acde1 |
| block-buffer | 0.10.4 | MIT OR Apache-2.0 | https://github.com/RustCrypto/utils/tree/6d35952d3d3b124bc1049ad6fb406b42b1ce4bfe |
| borrow-or-share | 0.2.4 | MIT-0 | https://github.com/yescallop/borrow-or-share/tree/fa67a43ce36367757ace1824434b9edaa53f5a09 |
| bytemuck | 1.25.2 | Zlib OR Apache-2.0 OR MIT | https://github.com/Lokathor/bytemuck/tree/f363643e951a7ac9e4b9921de982f2b0918902e3 |
| byteorder | 1.5.0 | Unlicense OR MIT | https://github.com/BurntSushi/byteorder/tree/ec068eefa042d494475db125c4b034bd8e9e34dd |
| cpufeatures | 0.2.17 | MIT OR Apache-2.0 | https://github.com/RustCrypto/utils/tree/9d92d5e95ab4c07c5d8bfd024bf2a17e96d20feb |
| ctor | 0.8.0 | Apache-2.0 OR MIT | https://github.com/mmastrac/rust-ctor/tree/f157640f88f958157371b39e83d85ec1a9d49cf2 |
| deranged | 0.5.8 | MIT OR Apache-2.0 | https://github.com/jhpratt/deranged/tree/7d0c671e8c806b96d582af197df3c620e09cb33b |
| digest | 0.10.7 | MIT OR Apache-2.0 | https://github.com/RustCrypto/traits/tree/344389411fd9718a0742435152e933a9e71461ee |
| dunce | 1.0.5 | CC0-1.0 OR MIT-0 OR Apache-2.0 | https://gitlab.com/kornelski/dunce/tree/1ee29a83526c9f4c3618e1335f0454c878a54dcf |
| equivalent | 1.0.2 | Apache-2.0 OR MIT | https://github.com/indexmap-rs/equivalent/tree/44cdd44f8b8ebb5f9ae096c7550a5e74ffb7d6ae |
| fnv | 1.0.7 | Apache-2.0 / MIT | https://github.com/servo/rust-fnv/tree/4b4784ebfd3332dc61f0640764d6f1140e03a9ab |
| futures-io | 0.3.34 | MIT OR Apache-2.0 | https://github.com/rust-lang/futures-rs/tree/705e6b5c0f06535b1aac1cb1989a172b3d45be8c |
| futures-sink | 0.3.34 | MIT OR Apache-2.0 | https://github.com/rust-lang/futures-rs/tree/705e6b5c0f06535b1aac1cb1989a172b3d45be8c |
| http-body-util | 0.1.5 | MIT | https://github.com/hyperium/http-body/tree/07838bd97b714b95bd783cd695ebf211b67545c4 |
| http-body | 1.1.0 | MIT | https://github.com/hyperium/http-body/tree/2fb78de9c875c364b7eb1a1a117acc3b83ffb13a |
| icu_normalizer_data | 2.3.0 | Unicode-3.0 | https://github.com/unicode-org/icu4x/tree/a14f2dad852be26bad277ae704abf27a15cbfed1 |
| icu_properties | 2.3.0 | Unicode-3.0 | https://github.com/unicode-org/icu4x/tree/a14f2dad852be26bad277ae704abf27a15cbfed1 |
| idna_adapter | 1.2.2 | Apache-2.0 OR MIT | https://github.com/hsivonen/idna_adapter/tree/1d9782f32c9e29218542b4a9411a82b35ec5c8cb |
| indexmap | 2.14.2 | Apache-2.0 OR MIT | https://github.com/indexmap-rs/indexmap/tree/41a870887c4c77adf665886e63df08f406bfe37a |
| keyboard-types | 0.7.0 | MIT OR Apache-2.0 | https://github.com/pyfisch/keyboard-types/tree/61a081f1e78a881a369abc22c3a0e37049bd655e |
| litemap | 0.8.3 | Unicode-3.0 | https://github.com/unicode-org/icu4x/tree/a14f2dad852be26bad277ae704abf27a15cbfed1 |
| lock_api | 0.4.14 | MIT OR Apache-2.0 | https://github.com/Amanieu/parking_lot/tree/d7828fff7b5d6327ae608e82db45f888b344449a |
| num-cmp | 0.1.0 | MIT/Apache-2.0 | https://crates.io/api/v1/crates/num-cmp/0.1.0/download |
| num-conv | 0.2.2 | MIT OR Apache-2.0 | https://github.com/jhpratt/num-conv/tree/b022fe87ac3ad5b0d7606ea7465549eaa92efe97 |
| num-traits | 0.2.19 | MIT OR Apache-2.0 | https://github.com/rust-num/num-traits/tree/7ec3d41d39b28190ec1d42db38021107b3951f3a |
| pin-project-lite | 0.2.17 | Apache-2.0 OR MIT | https://github.com/taiki-e/pin-project-lite/tree/3bdf763446aa78f90e3bdac1ef583e014832ab4c |
| serde_spanned | 1.1.1 | MIT OR Apache-2.0 | https://github.com/toml-rs/toml/tree/9db8aad6eafbc62f6b9d1950117649cc41eaf695 |
| siphasher | 1.0.3 | MIT/Apache-2.0 | https://github.com/jedisct1/rust-siphash/tree/451f67d73a772cba325728109bbfa247750ed076 |
| subtle | 2.6.1 | BSD-3-Clause | https://github.com/dalek-cryptography/subtle/tree/5457b5448b021d1da101ababbb854e6657233943 |
| sync_wrapper | 1.0.2 | Apache-2.0 | https://github.com/Actyx/sync_wrapper/tree/55413956c36aeab47feb8c04d1b7a044d6df336a |
| thiserror | 1.0.69 | MIT OR Apache-2.0 | https://github.com/dtolnay/thiserror/tree/41938bd3a03a70d34ed8e53d99c89c770c7c9c41 |
| thiserror | 2.0.20 | MIT OR Apache-2.0 | https://github.com/dtolnay/thiserror/tree/b1d5db5e039275d95bf7536a2b2192aeb4dc28bf |
| time-core | 0.1.9 | MIT OR Apache-2.0 | https://github.com/time-rs/time/tree/5d8737c39b9170c36c99cfc1f9f49cf0c059c63a |
| tinystr | 0.8.4 | Unicode-3.0 | https://github.com/unicode-org/icu4x/tree/a14f2dad852be26bad277ae704abf27a15cbfed1 |
| tower-layer | 0.3.3 | MIT | https://github.com/tower-rs/tower/tree/fec9e559e276ba9609f939d3b0d2e4fa0504de6f |
| tower-service | 0.3.3 | MIT | https://github.com/tower-rs/tower/tree/646804d77eebf072dac180cb5e1256b9ee7e0229 |
| try-lock | 0.2.5 | MIT | https://github.com/seanmonstar/try-lock/tree/fd160ecd9105e8afcc43dbea450a0ef6e5128cce |
| unic-char-property | 0.9.0 | MIT/Apache-2.0 | https://github.com/open-i18n/rust-unic//tree/5878605364af97a3358368a6eaef02104af2e016 |
| uuid-simd | 0.8.0 | MIT | https://github.com/Nugine/simd/tree/d74c030d9dc4f3cae02146d1f497ff62726ef09a |
| vsimd | 0.8.0 | MIT | https://github.com/Nugine/simd/tree/d74c030d9dc4f3cae02146d1f497ff62726ef09a |
| webview2-com-sys | 0.38.2 | MIT | https://github.com/wravery/webview2-rs/tree/b74dc5e2b394044bea5191052868ce7a106c202c |
| winapi-util | 0.1.11 | Unlicense OR MIT | https://github.com/BurntSushi/winapi-util/tree/803874c57dc1f10ecd42f7c86d9de72f53818432 |
| windows-result | 0.3.4 | MIT OR Apache-2.0 | https://github.com/microsoft/windows-rs/tree/49e5d37ef31838d027c41ee28d696e046d04c27f |
| windows-sys | 0.61.2 | MIT OR Apache-2.0 | https://github.com/microsoft/windows-rs/tree/32c3144490c016fe496a0aed769bce60987a2e9d |
| windows-version | 0.1.7 | MIT OR Apache-2.0 | https://github.com/microsoft/windows-rs/tree/32c3144490c016fe496a0aed769bce60987a2e9d |
| windows_x86_64_msvc | 0.53.1 | MIT OR Apache-2.0 | https://github.com/microsoft/windows-rs/tree/d468916ac27a36fb8a12bafc1bf5c0ec2fe92238 |
| writeable | 0.6.4 | Unicode-3.0 | https://github.com/unicode-org/icu4x/tree/a14f2dad852be26bad277ae704abf27a15cbfed1 |
| zeroize | 1.9.0 | Apache-2.0 OR MIT | https://github.com/RustCrypto/utils/tree/0b715735a660a8566ccd240bf42489fe2ed98efb |
| zerovec | 0.11.8 | Unicode-3.0 | https://github.com/unicode-org/icu4x/tree/c56bbb5a7b47409759113903764c456f13b418e5 |

### Linked native and toolchain support

| Component | Version | Terms | Source or original terms |
| --- | --- | --- | --- |
| Rust standard library/runtime | 1.98.1, compiler 48a229ceaefd4985c50990b14116b6d856af0985 | MIT OR Apache-2.0 | https://github.com/rust-lang/rust/tree/48a229ceaefd4985c50990b14116b6d856af0985/library |
| AWS-LC native code | aws-lc-sys 0.45.0 package payload | Original composite Apache/ISC/BSD/CC0/third-party terms in exact LICENSE | https://github.com/aws/aws-lc-rs/tree/aws-lc-sys-0.45.0 |
| SQLite amalgamation | 3.53.2, source id in exact original header/index | Public-domain blessing | https://sqlite.org/ |
| Rust compiler-builtins | 0.1.160, compiler 48a229ceaefd4985c50990b14116b6d856af0985 | MIT AND Apache-2.0 WITH LLVM-exception AND (MIT OR Apache-2.0) | https://github.com/rust-lang/rust/tree/48a229ceaefd4985c50990b14116b6d856af0985/library/compiler-builtins |
| Microsoft Visual C++ static release runtime | 14.51.36231 | Microsoft proprietary runtime/distributable-code terms | https://visualstudio.microsoft.com/license-terms/vs2026-ga-visualcpp-v14-redist-runtime/ ; https://visualstudio.microsoft.com/license-terms/vs2026-ga-pro-enterprise/ |
| Rust core/alloc inside nsis-tauri-utils | plugin toolchain version unpublished | MIT OR Apache-2.0 | https://github.com/rust-lang/rust/tree/master/library |

The linked Microsoft startup/runtime objects are distinct from Windows system
DLL imports. No separately installed VC Redistributable or full WebView2 Runtime
is embedded. The development SDK/compiler libraries are not download payloads.
This is a technical component/license audit, not a formal legal opinion.

### Retained generated frontend runtime modules

These are positively identified virtual modules in the final bundler output,
not an assertion that the entire build-tool dependency universe is distributed.
The private observer emits no application resources and does not change chunks.

| Component | Version | License | Original package/source |
| --- | --- | --- | --- |
| vite | 8.2.2 | MIT | https://www.npmjs.com/package/vite/v/8.2.2 |
| rolldown | 1.2.7 | MIT | https://www.npmjs.com/package/rolldown/v/1.2.7 |
| @oxc-project/runtime | 0.148.0 | MIT | https://www.npmjs.com/package/@oxc-project/runtime/v/0.148.0 |
| Babel runtime helper origin | upstream patch unpublished; copied in OXC 0.148.0 | MIT, original Babel attribution retained | https://github.com/babel/babel/blob/v7.28.4/LICENSE |


## PCKB 0.7.0 macOS attribution delta

The previously verified attribution set is retained. The following exact locked packages add source ZIP export and canonical Unicode path collision checking. ZIP default features are disabled; only Stored ZIP is used. No optional ZIP compression or encryption dependency is enabled. Historical Windows component notices do not imply a Windows 0.7.0 release.

| Component | Version | License | Exact upstream source |
| --- | --- | --- | --- |
| unicode-normalization | 0.1.25 | MIT OR Apache-2.0 | https://github.com/unicode-rs/unicode-normalization/tree/5a69b3bafb625caccdec7871a42bed0d9a6604d1 |
| zip | 8.6.0 | MIT | https://github.com/zip-rs/zip2/tree/771dfc534d2614158af5497ea3dff4d4208d7db1 |
| typed-path | 0.12.3 | MIT OR Apache-2.0 | https://github.com/chipsenkbeil/typed-path/tree/ec65f79eb1f61b0e11e70859b041a0a304c3a9ff |
| tinyvec | 1.13.2 | Zlib OR Apache-2.0 OR MIT | https://github.com/Lokathor/tinyvec/tree/5ae3e523dd46392d45f929591889430d1438ae5e |
| tinyvec_macros | 0.1.1 | MIT OR Apache-2.0 OR Zlib | https://github.com/Soveu/tinyvec_macros/tree/860c23a09d91c8b9203134a81de7888b7191d5f2 |

PCKB 0.7.1 attribution scope: this UI-only patch uses the same exact third-party dependency versions as 0.7.0. The verified component inventory and complete license texts are retained unchanged. No Windows binary is shipped in 0.7.1.
