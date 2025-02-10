# PurgeCSS and Dynamic Content in Tailwind CSS
This repository demonstrates an uncommon bug encountered when using PurgeCSS with Tailwind CSS and dynamically generated content.  PurgeCSS, while crucial for optimizing Tailwind CSS builds, may inadvertently remove CSS classes applied to elements added to the DOM after the initial render.

## The Problem
The core issue lies in PurgeCSS's static analysis.  If a class is not present in the initial HTML, PurgeCSS might eliminate it, even if it's later added via JavaScript. This leads to missing styles in dynamically created elements.

## Solution
The solution typically involves configuring PurgeCSS to understand and retain these dynamically added classes. This often requires specifying additional selectors or using techniques to ensure these classes are detected during the build process.  This repo showcases a solution using a more robust approach.