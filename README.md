# visay-keyboard-data

Language data packs for the **Visay** keyboard (Android IME and iOS keyboard extension): dictionaries used to type Chinese characters.

| Pack | Input | Data source | Data license |
|---|---|---|---|
| `kbpack-ja` | Japanese kana → kanji | [Mozc](https://github.com/google/mozc) `src/data/dictionary_oss` | BSD-3-Clause (Mozc) + IPAdic (NAIST) / ICOT Free Software notice + Okinawa Dictionary (public domain) — see [NOTICE](NOTICE) |
| `kbpack-zh-hans` | Simplified Chinese, pinyin | [AOSP PinyinIME](https://android.googlesource.com/platform/packages/inputmethods/PinyinIME) `rawdict_utf16_65105_freq.txt` | Apache-2.0 — see [NOTICE](NOTICE) |
| `kbpack-zh-hant` | Traditional Chinese, zhuyin / pinyin / Cangjie / Sucheng (Quick) | [McBopomofo](https://github.com/openvanilla/McBopomofo) (from libtabe) + [Unihan](https://www.unicode.org/charts/unihan.html) `kCangjie` | MIT / BSD + Unicode License v3 — see [NOTICE](NOTICE) |

The keyboard downloads only the pack for the language a user actually types. Packs are attached to [Releases](../../releases) together with a `pack.json` manifest (`sha256`, format version, licenses). The app verifies the checksum before using a pack.

Apps read the pack index for their format version from
`https://raw.githubusercontent.com/sandk-hub/visay-keyboard-data/main/index/v1.json`. Each pack entry has `url`, `gz_bytes`, `gz_sha256`, `bytes`, `sha256`, `data_version`, `licenses`. The app downloads the `.gz`, verifies both checksums, decompresses it once and memory-maps the result.

| Pack | Release |
|---|---|
| `kbpack-ja` | [`kbpack-ja-mozc-c7538e6f-c7000`](../../releases/tag/kbpack-ja-mozc-c7538e6f-c7000), 8.3 MB download, 16.5 MB on device |
| `kbpack-zh-hans` | [`kbpack-zh-hans-aosp-49aebad1-s400`](../../releases/tag/kbpack-zh-hans-aosp-49aebad1-s400), 1.2 MB download, 2.9 MB on device |
| `kbpack-zh-hant` | [`kbpack-zh-hant-mcbpmf-be6564ac-u18-s400-f2-sc`](../../releases/tag/kbpack-zh-hant-mcbpmf-be6564ac-u18-s400-f2-sc) (format v2 + Sucheng keys), 4.2 MB download, 13.1 MB on device |
