## 2024-05-18 - Missing Context on Prominent Floating Action Buttons
**Learning:** Prominent floating action buttons (like center bottom-nav icons) are often designed without visible text labels to maintain a clean aesthetic, but this severely degrades the experience for screen reader users by removing context completely.
**Action:** Always add `aria-label` (and often a standard tooltip via `title`) alongside appropriate focus indicators (`focus-visible`) for any interactive element that lacks visible text. Inner decorative icons should receive `aria-hidden="true"`.
## 2024-06-14 - Missing ARIA Roles for Custom UI Components
**Learning:** Custom UI components like toggle buttons and toast notifications that aren't native HTML elements often lack screen reader support. A `.tog` CSS class doesn't inherently communicate its switch functionality or on/off state to screen readers.
**Action:** When building custom interactive components, always provide an appropriate `role` (like `switch` or `status`) and dynamically manage their corresponding ARIA attributes (like `aria-checked` and `aria-live`) using JavaScript.
