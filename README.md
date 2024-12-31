# Tailwind CSS @apply Directive Issue with Pseudo-selectors

This repository demonstrates a bug where Tailwind CSS's `@apply` directive fails to apply styles when a pseudo-selector (e.g., `:hover`, `:focus`) is included in the class being applied.

## Bug Description

The `@apply` directive, intended for applying pre-defined styles, doesn't work as expected when combined with pseudo-selectors within the applied class.  This leads to the styles not appearing when the pseudo-selector condition is met.

## Reproduction

1. Clone this repository.
2. Open `bug.css`. You'll see a `.button` class attempting to apply hover styles using `@apply`.
3. Observe that the hover styles don't work.

## Solution

The solution is to apply the base styles separately and then apply the hover styles separately using the hover pseudo-class directly in the main CSS rather than relying on `@apply` for pseudo-selectors.

View `bugSolution.css` for the corrected implementation.