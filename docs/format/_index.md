---
title: NEP Format and Templates
description: NEP Format and Templates
---

This document will cover:

- NEP Document Directory

- NEP Header Preamble

- NEP Content Format

- NEP Templates


## I. NEP Document Directory

```
NEPs Root Directory
-------------------
.
└── NEPS
|   └── nep-x             // `x` is the NEP Number
|   |   └── index.md      // main NEP Document in English
|   |   └── index.zh.md   // main NEP Document in Chinese
|   |   ├── image1.png    // image used in NEP
|   |   ├── image2.jpg    // image used in NEP
|   |   └── filename.ext  // file used in NEP
```
### NEP Document File

NEP Doument file is `index.md` file in it's directory.

Every NEP should starts with the English version first. Each translation is translated from that English and placed in a new file using `index.lang.md` format.

### Auxiliary Files

If your NEP requires images, the image files should be included in the same directory of that NEP. When linking to an image in the NEP, use relative links such as `image.png`. Other files should follow the same pattern.

- When linking files from another NEP, it is enforced to copy that file from reference NEP directory to the working NEP directory.

- Files of `jpg`, `jpeg`, `png`, `svg` format are generally accepted.

- Files of `html`, `js` and other server-side or browser-side executable format are not accepted.

- If you must include an executable file like `js`, change the extension to `txt` instead.

## II. NEP Header Preamble

Here is an example of NEP Header Preamble, **all fields listed in this example are required**.

```
---
NEP: X
Title: "This is the NEP Title"
Authors: "[First Last](mailto:name@domain.ext)"
Discussions: https://url.to.discussions.ext
Status: Draft
Categories: Economic Model
Created: YYYY-MM-DD
---
```

### 1. NEP

-  _*required_
  
- NEP number (this is determined by the NEP editor)

### 2. Title

-  _*required_

- NEP title quoted with `" "`

### 3. Authors

-  _*required_

- A list of the author’s or authors’ name(s) and/or username(s), or name(s) and email(s). Details are below.

{{< details "Authors Examples" >}}
```
# Author with Email
Authors: "[First Last](mailto:name@domain.ext)"

# Author with URL
Authors: "[First Last](https://domain.ext)"

# Multiple Authors
Authors: "[Author 1](author1:name@domain.ext), [Author 2](https://author2.ext), [Author 3](mailto:aurhtor3@domain.ext)"
```
{{< /details >}}

### 4. Discussions

-  _*required_

- While an NEP is a draft, a discussions-to header will indicate the mailing list or URL where the NEP is being discussed.

- No Discussions header is necessary if the NEP is being discussed privately with the author and haven't been submitted to NEPs repo yet.

- Discussions **cannot** point to GitHub pull requests.

### 5. Status

-  _*required_

- WIP, Draft, Public Call, Final etc.

- See [NEP Status](../nep-status.md) for all available status

### 6. Categories

-  _*required_

- NEP currently has 5 categories: `Economic Model`, `Personnel`, `Technical`, `Community Governance` and `Business`

- This is defined by [NEP-0: NEP Genesis](../../NEPS/nep-0/index.md).

### 7. Created

- _*required_

- Date for first created in `YYYY-MM-DD` format

### 8. Updated

- Comma separated list of dates. 

- e.g. `2020-10-23` or `2020-10-23, 2020-11-01, 2020-12-13`

### 9. Types

- NEP currently has 3 types: `Standard Track`, `NRC` and `Informational`

### 10. SupersededBy

- The NEP Number of NEP that superseded this NEP.

- Only NEPs moved to `Active`, `Final` and later status can be added as an SupersededBy item.

### 11. Superseding

- The NEP Number of NEP that _is_ or _is to be_ superseded by this NEP

### Ordering

The order of NEP Header Preamble Item is not enforced, but it is recommended to use the order as the example below:

```
---
NEP: 
Title: 
Authors: 
Discussions: 
Status: 
SupersededBy: 
Superseding: 
Categories: 
Types: 
Created: 
Updated: 
---
```

## III. NEP Content Format

NEP Content should be written in **Markdown** format. Markdown formatting is widely used in websites and documents, also there were dozens of implementations in many languages and software applications. 

**CommonMark Spec** is a standard for Markdown and adopted by many applications. To see the latest **CommonMark Spec** please visit [https://spec.commonmark.org](https://spec.commonmark.org).

## VI. NEP Templates

NEP Template for Token (NRC)