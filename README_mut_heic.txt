Mutated HEIF test files created for parser testing.
Files:
- mut_heic_1.heic : contains a nested box with an intentionally incorrect large size (truncated payload).
- mut_heic_2.heic : contains a large EXIF-like metadata block (~500KB) to stress metadata parsers.
- mut_heic_3.heic : corrupt ftyp compatible brand bytes and some UTF-8 emoji in metadata.
Notes:
- These are synthetic containers (not full valid HEIC images). They are intended for fuzzing/parser testing and may be rejected by strict decoders.
- Host them on static hosting (e.g., GitHub Pages raw link) and open on the target iPhone Air in Safari, Mail, Files, or Photos to exercise different code paths.
- When reproducing, run `log stream` on the device with predicates for QuickLook/WebKit/mediaserverd as discussed.
