# CSS

## Table of Contents

| No. | Questions                                                                                                                                                                                       |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is CSS selector specificity and how does it work?](#what-is-css-selector-specificity-and-how-does-it-work)                                                                                |
| 2   | [What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?](#whats-the-difference-between-resetting-and-normalizing-css-which-would-you-choose-and-why) |
| 3   | [Describe `float`s and how they work.](#describe-floats-and-how-they-work)                                                                                                                      |
| 4   | [Describe `z-index` and how stacking context is formed.](#describe-z-index-and-how-stacking-context-is-formed)                                                                                  |
| 5   | [Describe BFC (Block Formatting Context) and how it works.](#describe-bfc-block-formatting-context-and-how-it-works)                                                                            |
| 6   | [Explain CSS sprites.](#explain-css-sprites)                                                                                                                                                    |
| 7   | [Types of @media property.](#types-of-media-property)                                                                                                                                           |
| 8   | [What are some of the "gotchas" for writing efficient CSS?](#what-are-some-of-the-gotchas-for-writing-efficient-css)                                                                            |
| 9   | [How would you implement a web design comp that uses non-standard fonts?](#how-would-you-implement-a-web-design-comp-that-uses-non-standard-fonts)                                              |
| 10  | [Explain how a browser determines what elements match a CSS selector.](#explain-how-a-browser-determines-what-elements-match-a-css-selector)                                                    |

1. ### What is CSS selector specificity and how does it work?

<details>
<summary>answer</summary>

#### useful links

- [mdn specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)

</details>

**[⬆ Back to Top](#table-of-contents)**

---

2. ### What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?

<details>
<summary>answer</summary>

- _Resetting_ - is meant to strip all default browser styling.
- _Normalizing_ - preserves useful default styles.

</details>

**[⬆ Back to Top](#table-of-contents)**

---

3. ### Describe `float`s and how they work.

<details>
<summary>answer</summary>

Flex is a CSS positioning property. Floated elements remain as part of the flow
of the page, and will affect the positioning of other elements, unlike
`position: absolute` elements, which are removed from the flow of the page.

</details>

**[⬆ Back to Top](#table-of-contents)**

---

4. ### Describe `z-index` and how stacking context is formed.

<details>
<summary>answer</summary>

The `z-index` property in CSS controls the vertical stacking order of elements
that overlap. `z-index` only affects elements that have a `position` value which
is not `static`. Without any `z-index` value, elements stack in the order that
they appear in the DOM.

</details>

#### useful links

- [mdn the stacking context](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context)

**[⬆ Back to Top](#table-of-contents)**

---

5. ### Describe BFC (Block Formatting Context) and how it works.

<details>
<summary>answer</summary>

#### useful links

- [mdn BFC](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Block_formatting_context)
- [so How does the CSS Block Formatting Context work?](https://stackoverflow.com/questions/6196725/how-does-the-css-block-formatting-context-work)

</details>

**[⬆ Back to Top](#table-of-contents)**

---

6. ### Explain CSS sprites.

<details>
<summary>answer</summary>

#### useful links

- [mdn Implementing image sprites in CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Images/Implementing_image_sprites_in_CSS)

</details>

**[⬆ Back to Top](#table-of-contents)**

---

7. ### Types of @media property.

<details>
<summary>answer</summary>

#### useful links

- [mdn @media](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#media_types)

</details>

**[⬆ Back to Top](#table-of-contents)**

---

8. ### What are some of the "gotchas" for writing efficient CSS?

<details>
<summary>answer</summary>

Understand that browsers match selectors from rightmost (key selector) to left.
Browsers filter out elements in the DOM according to the key selector and
traverse up its parent elements to determine matches. The shorter the length of
the selector chain, the faster the browser can determine if that element
matches the selector. Hence avoid key selectors that are tag and universal
selectors. They match a large number of elements and browsers will have to do
more work in determining if the parent do match.

Be aware of which CSS properties trigger reflow, repaint, and compositing.
Avoid writing styles that change the layout (trigger reflow) where possible.

</details>

**[⬆ Back to Top](#table-of-contents)**

---

9. ### How would you implement a web design comp that uses non-standard fonts?

<details>
<summary>answer</summary>

Use `@font-face` and define `font-family` for different `font-weight`s.

</details>

**[⬆ Back to Top](#table-of-contents)**

---

10. ### Explain how a browser determines what elements match a CSS selector.

<details>
<summary>answer</summary>

Browsers match selectors from rightmost (key selector) to left. Browsers filter
out elements in the DOM accodring to the key selector and traverse up its
parent elements to determine matches. The shorter the length of the selector
chain, the faster the browser can determine if that element matches the
selector.

For example with this selector `p span`, browsers firstly find all the `<span>`
elements and traverse up its parent all the way up to the root to find the
`<p>` element. For a particular `<span>`, as soon as it find a `<p>`, it knows
that the `<span>` matches and can stop its matching.

</details>

**[⬆ Back to Top](#table-of-contents)**

---
