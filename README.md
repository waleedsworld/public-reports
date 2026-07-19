# public-reports

An archived index of **publicly disclosed HackerOne reports** — a plain-text list of report
URLs paired with their public titles, spanning HackerOne's early reports through the
~one-millionth report ID.

> **Provenance / attribution.** This repository is a **fork/archive of a third-party dataset**.
> The report index was originally compiled and published by
> [**phlmox**](https://github.com/phlmox) in [`phlmox/public-reports`](https://github.com/phlmox/public-reports).
> The underlying data — report IDs, URLs, and titles — is drawn from
> [**HackerOne Hacktivity**](https://hackerone.com/hacktivity), HackerOne's public feed of
> disclosed reports. All report content, titles, and trademarks belong to their respective
> authors, programs, and HackerOne, Inc. See [`NOTICE`](./NOTICE) for full attribution and terms.
>
> This copy is retained here only as an archival mirror. It is **not** an original work of this
> account, and nothing here was authored, discovered, or claimed by the maintainer of this fork.

## What's in here

- **`hackerone-one-million-reports`** — the dataset. One report per line, in the form:

  ```
  https://hackerone.com/reports/<id> |  <public report title>
  ```

  Roughly 3,500 entries, ordered by ascending report ID.

## What it's useful for

The list is a lightweight, greppable index into HackerOne's public disclosure history — handy for
security researchers and learners who want to browse real-world vulnerability write-ups by keyword
without hitting the site's search UI. For example:

```bash
# find disclosed SSRF reports
grep -i 'ssrf' hackerone-one-million-reports

# count reports mentioning "account takeover"
grep -ic 'account takeover' hackerone-one-million-reports

# open a report by ID
grep '/reports/12345 ' hackerone-one-million-reports
```

Every link points to a report on `hackerone.com`; the write-ups themselves live on HackerOne, not
in this repository.

## Freshness

This is a point-in-time snapshot (the source data dates to early 2021 and stops around report ID
~1,002,000). It is **not** kept in sync with new HackerOne disclosures. For live data, use
[HackerOne Hacktivity](https://hackerone.com/hacktivity) directly.

## License / usage

The index is aggregated public metadata. Report titles and links are the property of their
respective authors and of HackerOne, Inc. Treat this archive as reference material and honor
HackerOne's terms of service when using it. See [`NOTICE`](./NOTICE).
