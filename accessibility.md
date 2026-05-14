---
title: Accessibility
---

![Accessibility Score](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/berkeley-cdss/course-site-myst/badges/a11y-badge.json)

As noted in the [MyST documentation](https://mystmd.org/guide/accessibility-and-performance), "The default MyST web themes aim to meet WCAG 2.1 AA, the level required of US public-sector and many private websites under ADA Title II."

## Accessible by Default

MyST generates semantic HTML that is highly compatible with screen readers and assistive technologies. Key built-in accessibility features include:
* **Semantic Structure**: Proper heading hierarchies, lists, and article structures are automatically generated, making navigation easier.
* **Accessible Math**: Mathematical equations are rendered in ways that assistive technologies can readily interpret.
* **Interactive Elements**: UI components like dropdowns, admonitions, and tabs are built with appropriate ARIA roles and keyboard navigation support.
* **High Contrast**: The default themes are designed with sufficient color contrast for readability.

## Automated Accessibility Testing (CI/CD)

To ensure that this course website remains accessible as content is added or modified by instructors, we employ automated accessibility testing through GitHub Actions.

Our Continuous Integration (CI) workflow (`.github/workflows/a11y.yml`) runs automatically whenever changes are pushed to the repository. It tries to ensure that high accessibility standards are maintained by performing the following steps:

1. **Builds the Site**: Compiles the MyST Markdown into static HTML.
2. **Discovers Pages**: Identifies all generated `.html` files in the build output.
3. **Runs Axe-Core**: Utilizes the industry-standard [@axe-core/cli](https://github.com/dequelabs/axe-core-npm/tree/develop/packages/cli) to aggressively evaluate each page against **WCAG 2.0** and **WCAG 2.1 Level A and AA** standards.
4. **Updates the Badge**: Calculates an overall accessibility score based on the ratio of passing checks to violations, and dynamically updates the badge displayed in the README.md. This page happens to contains the same badge, but this is for demonstration purposes.

This automated safety net helps authors continuously catch and fix accessibility issues before they ever reach the students.
