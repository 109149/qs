# HTML

## Table of Contents

| No. | Questions                                                                                                                                                       |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|     | **HTML**                                                                                                                                                        |
| 1   | [What does a doctype do?](#what-does-a-doctype-do)                                                                                                              |
| 2   | [How do you serve a page with content in multiple languages?](#how-do-you-serve-a-page-with-content-in-multiple-languages)                                      |
| 3   | [What are `data-` attributes good for?](#what-are-data--attributes-good-for)                                                                                    |
| 4   | [Consider HTML5 as an open web platform. What are the building blocks of HTML5?](#consider-html5-as-an-open-web-platform-what-are-the-building-blocks-of-html5) |
| 5   | [Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.](#describe-the-difference-between-a-cookie-sessionstorage-and-localstorage)   |

## Questions and Answers

1. ### What does a doctype do?

<details>
<summary>answer</summary>

`<!DOCTYPE html>` is (required) preamble found at the top of the documents. Its
purpose is to prevent browser from switching into so-called "quirk-modes" when
rendering a document; that is, the `<!DOCTYPE html>` doctype ensures that the
browser makes a best-effort attempt at following the relevant specifications.

</details>

**[⬆ Back to Top](#table-of-contents)**

---

2. ### How do you serve a page with content in multiple languages?

<details>
<summary>answer</summary>

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

---

3. ### What are `data-` attributes good for?

<details>
<summary>answer</summary>

`data-` can be helpful when we are testing e2e.

</details>

**[⬆ Back to Top](#table-of-contents)**

---

4. ### Consider HTML5 as an open web platform. What are the building blocks of HTML5?

<details>
<summary>answer</summary>

- _Semantincs_: allowing you to describe more precisely what your content is.
- _Connectivity_: allowing you to communicate with the server.
- _Offline & storage_: allowing webpages to store data on the client-side
  locally and operate offline.
- _Multimedia_
- _2D/3D graphics and effects_
- _Performance and integration_
- _Device access_
- _Styling_

</details>

#### useful links

- [mdn HTML5](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)

**[⬆ Back to Top](#table-of-contents)**

5. ### Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.

<details>
<summary>answer</summary>

|                                        | `cookie`                                             | `localStorage` | `sessionStorage` |
| -------------------------------------- | ---------------------------------------------------- | -------------- | ---------------- |
| Initiator                              | Client or server. Server can use `Set-Cookie` header | Client         | Client           |
| Expiry                                 | Custom                                               | Never          | On tab close     |
| Persistent across browser sessions     | Custom                                               | Yes            | No               |
| Sent to server with every HTTP request | Cookies are automatically sent via `Cookie` header   | No             | No               |
| Capacity (per domain)                  | 4kb                                                  | 5MB            | 5MB              |
| Accessiblity                           | Any window                                           | Any window     | Same tab         |

</details>

**[⬆ Back to Top](#table-of-contents)**

---
