This is an example document of the files created for the company's internal Confluence documentation. Some information has been stripped, and examples removed.

# Testing Guides & Key Concepts  
### Accessibility Testing Framework (WCAG 2.1 & 2.2)

## Overview

Accessibility testing ensures that all users—including those with visual, auditory, motor, or cognitive disabilities—can successfully navigate and interact with Level Data products. Automated tools can identify predictable issues, but **manual testing is essential** for evaluating context, meaning, workflow logic, and user experience.

The following sections break down the core testing methods and key concepts required for comprehensive accessibility evaluation.

---

# 1. Automated Scans

Automated scanning tools provide a fast, high‑level assessment of potential accessibility issues. They are an important first step but **cannot replace manual testing**.

### Objectives
- Identify predicted issues related to ARIA attributes, structure, and keyboard focus.
- Re‑scan the page every time the UI changes, including when:
  - A modal opens  
  - A dropdown is selected  
  - Buttons or links become enabled/disabled  

> Scans pages for predicted accessibility issues. Note: does not replace manual testing.

### Tips
- Keep DevTools docked to the **bottom** of the screen to avoid altering page layout.
- Use automated results as a **starting point**, not a final verdict.

---

# 2. Screen Reader Testing

Screen reader testing validates how non‑visual users experience the page.

### Objectives
Ensure that:

- Content is announced in a **logical reading order**
- Essential images have meaningful **alt text**
- Labels, names, and units of measurement are fully announced
- Interactive elements provide clear, descriptive names

> A video demonstrating screen reader behavior in the context of the product was provided during training.

---

# 3. Keyboard‑Only Navigation

Keyboard accessibility is a core WCAG requirement and essential for users who cannot use a mouse.

### Objectives
Ensure that:

- All functionality available by mouse is also operable via keyboard
- Focus order is logical and predictable
- Focus indicators are visible
- Focus never becomes “trapped” in an element

### Tips
- Use the **ANDI bookmarklet** to visualize tab order when debugging focus issues.

---

# 4. Touchscreen Interaction

Touchscreen testing ensures that workflows remain functional across input methods.

### Objectives
- Switching between touch and keyboard should **not disrupt workflow**
- Focus indicators should remain consistent
- Dropdowns, modals, and interactive components must behave predictably

> Open a dropdown using touch → make a selection using keyboard → workflow should remain intact.

---

# 5. ANDI Bookmarklet

ANDI is a multi‑functional inspection tool for evaluating accessible markup.

### Objectives
- Inspect elements for accessible names, roles, and structure
- Validate ARIA attributes
- Identify missing or incorrect markup

### Tips
- At **200% zoom**, enable **Minimode** so the ANDI interface takes up less space.

---

# 6. Contrast Checking

Color contrast is essential for users with low vision or color‑perception differences.

### Objectives
- Verify text and UI elements meet WCAG contrast ratios
- Use HEX codes or the eyedropper tool to compare foreground/background colors

> Tests the contrast ratio between text and background to ensure visibility for low‑vision users.

---

# 7. Why Manual Testing Matters

Automated tools are helpful, but they cannot evaluate:

- Context or meaning  
- Whether content is decorative or essential  
- Pronunciation of abbreviations or unique terms  
- Multi‑input workflows (touch → keyboard → mouse)  
- Whether multiple methods exist to complete a task  

> Manual testing ensures the product is accessible in **real‑world use**, not just in theory.

---

# 8. Testing All Page States

Accessibility must be validated across **every state** of a page, including:

- Enabled/disabled elements  
- Modals and alerts  
- Returned states (e.g., after submitting a form)  
- Generated documents (PDFs, CSVs, etc.)  
- Multiple browsers  
- 200% and 400% zoom  

> This ensures full compliance with WCAG’s expectations for **complete processes**, not just static pages.

---

# 9. Documentation & Communication of Findings

Clear documentation ensures issues are understood, prioritized, and resolved efficiently.

### Best Practices
- Link each issue to the relevant **WCAG Success Criterion**
- Include links to W3C patterns, practices, and understanding docs
- Use spreadsheets or guiding documents for tracking
- Create Epics/Parent Issues for accessibility work
- Ensure Product Owners and Engineering Managers have visibility into:
  - Team capacity  
  - Complexity of fixes  
  - Priority relative to other work  

> Tickets should contain links to the relevant WCAG Success Criteria… and other relevant resources.

---

# 10. VPAT‑Specific Testing

VPAT evaluations require a deeper level of rigor.

### Key Concepts
- VPATs are **not checklists**
- Each criterion must be evaluated across **every page, component, and state**
- A criterion is “fully supported” only if at least one accessible method exists throughout the entire product
- VPATs document **criteria**, not specific product defects

> This makes VPATs unsuitable for tracking fixes, but essential for compliance reporting.

---

# 11. Summary

The Testing Guides & Key Concepts outlined here form the foundation of Level Data’s accessibility testing approach. By combining automated tools, manual evaluation, and cross‑functional collaboration, teams can ensure that products meet WCAG 2.1 and 2.2 standards and provide equitable access for all users.

These guidelines were developed collaboratively by the **Product Owner/Technical Writer** and the **QA Accessibility SME**, then expanded into a full Confluence documentation system to support company‑wide adoption.

