# HTML

## Table of Contents

| No. | Questions                                                                                                                   |
| --- | --------------------------------------------------------------------------------------------------------------------------- |
|     | **HTML**                                                                                                                    |
| 1   | [What does a doctype do?](#what-does-a-doctype-do)                                                                          |
| 2   | [How do you serve a page with content in multiple languages?](#how-do-you-serve-a-page-with-content-in-multiple-languages?) |

## Questions and Answers

1. ### What does a doctype do?

<details>
<summary>ANSWER</summary>

`<!DOCTYPE html>` is (required) preamble found at the top of the documents. Its
purpose is to prevent browser from switching into so-called "quirk-modes" when
rendering a document; that is, the `<!DOCTYPE html>` doctype ensures that the
browser makes a best-effort attempt at following the relevant specifications.

</details>

**[⬆ Back to Top](#table-of-contents)**

2. ### How do you serve a page with content in multiple languages?

<details>
<summary>ANSWER</summary>

`Accept-Language` request header.
`Content-Language` response header.

default value for `lang` attribute is `unknown`, it is recommended to always
specify this attribute with appropriate value `<html lang="...">...</html>`.

for seo:

```html
<link rel="alternate" hreflang="en-gb" href="..." />
```

</details>

**[⬆ Back to Top](#table-of-contents)**
