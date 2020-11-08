---
layout: default
---

# Extract Attachments

This command extracts attachments from a PDF document. 
If you want to remove an extracted document you can do this using [attach remove](attach_remove.md). Have a look at some [examples](#examples).

## Usage

```
pdfcpu attachments extract [-v(erbose)|vv] [-q(uiet)] [-upw userpw] [-opw ownerpw] inFile outDir [file...]
```

<br>

### Flags

| name                                          | description       | required
|:----------------------------------------------|:------------------|:--------
| [verbose](../getting_started/common_flags.md) | turn on logging   | no
| [vv](../getting_started/common_flags.md)      | verbose logging   | no
| [quiet](../getting_started/common_flags.md)   | quiet mode        | no
| [upw](../getting_started/common_flags.md)     | user password     | no
| [opw](../getting_started/common_flags.md)     | owner password    | no

<br>

### Arguments

| name         | description         | required
|:-------------|:--------------------|:--------
| inFile       | PDF input file      | yes
| outDir       | output directory    | yes
| file...      | one or more attachments to be extracted | yes

<br>

## Examples

Extract a specific attachment from `ledger.pdf` into `out`:

```sh
pdfcpu attach extract ledger.pdf out invoice1.pdf
writing out/invoice.pdf
```

<br>

Extract all attachments of `ledger.pdf` into `out`:

```sh
pdfcpu attach extract ledger.pdf out *
writing out/invoice1.pdf
writing out/invoice2.pdf
writing out/invoice3.pdf
```
