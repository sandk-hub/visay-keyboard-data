# visay-keyboard-data

Language data packs for the **Visay** keyboard (Android IME and iOS keyboard extension): dictionaries used to type Chinese characters.

| Pack | Input | Data source | Data license |
|---|---|---|---|
| `kbpack-ja` | Japanese kana → kanji | [Mozc](https://github.com/google/mozc) `src/data/dictionary_oss` | BSD-3-Clause (Mozc) + IPAdic (NAIST) / ICOT Free Software notice + Okinawa Dictionary (public domain) — see [NOTICE](NOTICE) |
| `kbpack-zh-hans` | Simplified Chinese, pinyin | planned: AOSP PinyinIME dictionary | Apache-2.0 |
| `kbpack-zh-hant` | Traditional Chinese, zhuyin / pinyin / Cangjie | planned: McBopomofo (libtabe) + rime-cangjie | MIT / BSD + **LGPL-3.0** (Cangjie table — source and build steps will be published here) |

The keyboard downloads only the pack for the language a user actually types. Packs are attached to [Releases](../../releases) together with a `pack.json` manifest (`sha256`, format version, licenses). The app verifies the checksum before using a pack.

Status: the Japanese pack format is in a measurement spike. No release has been published yet.
