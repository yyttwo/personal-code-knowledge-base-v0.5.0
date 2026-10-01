# Open-source license bundle

This directory contains only license, copyright, attribution, and public-domain evidence mapped to components actually present in the frozen PCKB candidate.

`LICENSE_INDEX.tsv` maps every component to one or more exact evidence files. Identical files are stored once by SHA-256 and referenced by multiple component rows.

Baseline: the verified PCKB 0.3.0 runtime bundle, plus the audited 0.4.0 image-decoding dependency delta.

The component index includes the upstream objc2-family license text and its Apple SDK derivation notice. The notice records upstream uncertainty and does not state that redistribution is either legally confirmed or illegal.

Windows preparation adds only confirmed candidate component mappings and exact
upstream license texts. Identical content is reused by SHA-256; license text
line endings are normalized to LF, with a final newline. The original macOS
notice set is retained. The candidate uses NSIS LZMA, not the bzip2 or zlib
compression modules; only the relevant NSIS copyright/license/exception sections
are retained for that delta.

The Windows static-link contribution map and installed legal-file delivery are
not yet fully verified. This folder must not be treated as a complete Windows
release-compliance declaration. No objc2 risk-resolution claim is made.
