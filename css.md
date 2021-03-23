# CSS

## Table of Contents

| No. | Questions                                                                                                                                                                                       |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is CSS selector specificity and how does it work?](#what-is-css-selector-specificity-and-how-does-it-work)                                                                                |
| 2   | [What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?](#whats-the-difference-between-resetting-and-normalizing-css-which-would-you-choose-and-why) |
| 3   | [Describe `float`s and how they work.](#describe-floats-and-how-they-work)                                                                                                                      |
| 4   | [Describe `z-index` and how stacking context is formed.](#describe-z-index-and-how-stacking-context-is-formed)                                                                                  |

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
