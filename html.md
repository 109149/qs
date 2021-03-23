# HTML

## Table of Contents

| No. | Questions                                                                                                                                                                                                                                                                                     |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|     | **HTML**                                                                                                                                                                                                                                                                                      |
| 1   | [What does a doctype do?](#what-does-a-doctype-do)                                                                                                                                                                                                                                            |
| 2   | [How do you serve a page with content in multiple languages?](#how-do-you-serve-a-page-with-content-in-multiple-languages)                                                                                                                                                                    |
| 3   | [What are `data-` attributes good for?](#what-are-data--attributes-good-for)                                                                                                                                                                                                                  |
| 4   | [Consider HTML5 as an open web platform. What are the building blocks of HTML5?](#consider-html5-as-an-open-web-platform-what-are-the-building-blocks-of-html5)                                                                                                                               |
| 5   | [Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.](#describe-the-difference-between-a-cookie-sessionstorage-and-localstorage)                                                                                                                                 |
| 6   | [Describe the difference between `<script>`, `<script async>` and `<script defer>`.](#describe-the-difference-between-script-script-async-and-script-defer)                                                                                                                                   |
| 7   | [Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?](#why-is-it-generally-a-good-idea-to-position-css-links-between-headhead-and-js-scripts-just-before-body-do-you-know-any-exceptions) |
| 8   | [What is progressive rendering?](#what-is-progressive-rendering)                                                                                                                                                                                                                              |
| 9   | [Why you would use a `srcset` attribute in an image tag?](#why-you-would-use-a-srcset-attribute-in-an-image-tag)                                                                                                                                                                              |

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

---

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

6. ### Describe the difference between `<script>`, `<script async>` and `<script defer>`.

<details>
<summary>answer</summary>

- `<script>` - HTML parsing is blocked, script is fetched and executed
  immediately, HTML parsing resumes after the script is finished.
- `<script async>` - The script will be fetched in parallel to HTML, parsing
  and executing as soon as available (potentially before HTML parsing
  completes). Use `async` when there is no dependence between it and other
  scripts, like analytics.
- `<script defer>` - The script will be fetched in parallel to HTML, parsing
  and executing when the page has finished parsing. If there are multiple of
  them, each deferred script is executed in the order they were encountered in
  the document. If a script relies on fully parsed DOM, the `defer` attribute
  will be useful in ensuring that the HTML is fully parsed before executing. A
  deferred script must not contain `document.write`.

`async` and `defer` keywords are ignored for scripts that do not have `src`
attribute.

</details>

#### useful links

- [async vs defer attributes](https://www.growingwiththeweb.com/2014/02/async-vs-defer-attributes.html)

**[⬆ Back to Top](#table-of-contents)**

---

7. ### Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?

<details>
<summary>answer</summary>

Putting `<link>`s in the `<head>` is part of proper specification in building an
optimized website. When a page first loads, HTML and CSS are being parsed
simultaneously; HTML creates the DOM (Document Object Model) and CSS creates the
CSSOM (CSS Object Model). Both are needed to create the visuals in a website.
Some browsers block rendering to avoid having to repaint elements of the page if
their style changes, the user is stuck viewing a blank white page. Other times
there can be flashes of unstyled content (FOUC), which show a webpage with no
styling applied.
`<script>` blocks HTML parsing white they are being downloaded and executed
which can slow down page. Placing script at the bottom will allow the HTML to be
parsed and displayed to the user first.

</details>

**[⬆ Back to Top](#table-of-contents)**

---

8. ### What is progressive rendering?

<details>
<summary>answer</summary>

Progressive rendering is the name givern to techniques used to improve the
performance of a webpage to render content for display as quickly as possible.

Examples of such techniques:

- Lazy loading of images
- Prioritizing visible content
- Async HTML fragments

</details>

#### useful links

- [async fragments](https://tech.ebayinc.com/engineering/async-fragments-rediscovering-progressive-html-rendering-with-marko/)

**[⬆ Back to Top](#table-of-contents)**

---

9. ### Why you would use a `srcset` attribute in an image tag?

<details>
<summary>answer</summary>

You would use the `srcset` attribute when you wanto to serve different images to
users depending on their device width.

</details>

**[⬆ Back to Top](#table-of-contents)**

---
