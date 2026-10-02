# Indian exam photo & signature specs, quoted from the official documents

Photo and signature upload rules for five Indian exam portals: CTET, SSC,
NEET, JEE Main and UPSC. Every number here was taken from the conducting
body's own notification or instructions, and the exact sentence it came from
is stored next to it in `quotes`.

Most pages that list these specs copy each other. This one doesn't: if a number
isn't inside a quoted sentence from the official source, it isn't in the data.

## Use it

`exam-photo-specs.json` holds one object per exam:

| Field | What it is |
|---|---|
| `photo`, `signature` | `minKb`, `maxKb`, `dimensions`, `format`, only where the source states them. A missing field means the source does not say. |
| `quotes` | The official sentences the numbers come from, verbatim. |
| `source.url` | The official document. |
| `source.archivedCopy` | Set when the body has taken the original down (UPSC removed its instructions PDF in September 2026; this points to the Internet Archive's capture). |
| `verifiedOn` | The date the quotes were last checked against the source. |
| `page` | A readable page per exam, with a tool that resizes to the spec. |

Things the data shows that most guides get wrong:

- **SSC has no photo upload.** The photo is captured live. Any "SSC photo size" in KB is invented.
- **The minimum size rejects people too.** NTA forms (NEET, JEE Main) reject a signature under 10 KB.
- **UPSC rules aren't only about size.** The files must be named `photo` and `signature`, and the signature is signed three times on one sheet.

## Specs change every exam cycle

Check `verifiedOn`, then confirm against your own session's notification
before you upload. If an official document has changed, open an issue with
the link and the new sentence.

## Source and license

Maintained by [Docexp](https://docexp.com), free browser tools for form
uploads. Data licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/):
reuse it anywhere, credit "Docexp (docexp.com)".

The quoted sentences belong to the conducting bodies and are reproduced so
each figure can be checked against its source.
