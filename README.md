# onnxruntime-binaries

Byte-identical mirror of the ONNX Runtime iOS/macOS pod archives used by the Vibe iOS app's
vendored Swift package (`apps/ios/Packages/onnxruntime-spm` in vibeus/chorus).

The upstream host `download.onnxruntime.ai` stopped serving these files in November 2026
(its Azure CDN endpoint now presents a `*.azureedge.net` certificate and the origin returns 404),
and `github.com/microsoft/onnxruntime` is no longer available. The archives here were taken from
a SwiftPM cache populated from the original URLs, and their SHA-256 matches the checksums that
SwiftPM pins, so any modification would be rejected at resolve time.

| File | Release | SHA-256 |
| --- | --- | --- |
| `pod-archive-onnxruntime-c-1.24.2.zip` | `onnxruntime-1.24.2` | `f7100a992d2a8135168c8afd831e6a58b465349101982aa58b3e11d36e600b54` |
| `pod-archive-onnxruntime-extensions-c-0.13.0.zip` | `onnxruntime-1.24.2` | `346522d1171d4c99cb0908fa8e4e9330a4a6aad39cd83ce36eb654437b33e6b5` |

ONNX Runtime and ONNX Runtime Extensions are © Microsoft Corporation and licensed under the
MIT License; each archive includes its original `LICENSE` file. Do not add or modify files in
existing releases — publish a new release for new versions.
