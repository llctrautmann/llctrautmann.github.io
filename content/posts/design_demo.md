---
title: "Design Elements Demo"
date: 2025-01-01
tags: ["demo", "design"]
draft: true
---

This is a demo page showcasing all the different text elements and styles used on this site.

## Introduction

This page demonstrates various markdown elements to help visualize the design. It includes headings, text formatting, blockquotes, code blocks, lists, tables, and mathematical equations.

### Subsection Example

Here's a third-level heading with some regular paragraph text. The quick brown fox jumps over the lazy dog. This sentence contains all letters of the alphabet and helps demonstrate font rendering.

#### Fourth Level Heading

Even deeper nesting is possible with fourth-level headings.

##### Fifth Level Heading

And fifth-level headings too.

## Text Formatting

You can use **bold text** for emphasis, *italic text* for subtle emphasis, and ***bold italic text*** for strong emphasis. You can also use `inline code` for technical terms or code snippets.

Here's a longer paragraph to show how body text flows. Japanese design principles emphasize simplicity, asymmetry, and naturalness. The concept of "ma" (間) refers to negative space and the intervals between things. This breathing room is essential to minimalist aesthetics.

## Blockquotes

Here's a standard blockquote to showcase the new minimal design:

> This is a blockquote. It should now have a clean, minimal appearance with just a subtle left border and no background color. The text should be regular (not italic) and have plenty of breathing room.

> This is another blockquote with multiple lines of text. It demonstrates how longer quoted text appears with the new styling. Notice the elegant simplicity and how it doesn't interrupt the reading flow.

## Lists

### Unordered List

- First item
- Second item
- Third item
  - Nested item
  - Another nested item
- Fourth item

### Ordered List

1. First step
2. Second step
3. Third step
   1. Nested step
   2. Another nested step
4. Fourth step

## Code Blocks

Here's an inline code example: `const x = 42;`

And here's a block of Python code:

```python
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)

# Generate first 10 Fibonacci numbers
for i in range(10):
    print(f"F({i}) = {fibonacci(i)}")
```

Here's some JavaScript:

```javascript
const greet = (name) => {
  console.log(`Hello, ${name}!`);
};

greet("World");
```

## Links

Here's a [link to the homepage](/), and here's an [external link](https://example.com).

## Mathematical Equations

This site supports LaTeX math rendering. Here's an inline equation: \(E = mc^2\)

Here are block equations:

\[
\nabla \cdot \mathbf{E} = \frac{\rho}{\epsilon_0}
\]

$$
\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
$$

More complex equation:

\[
\frac{\partial u}{\partial t} = \alpha \nabla^2 u + f(x,t)
\]

## Tables

| Feature | Before | After |
|---------|--------|-------|
| Background | Beige | Transparent |
| Border | 3px | 2px |
| Text Style | Italic | Regular |
| Spacing | Standard | Enhanced |

## Images

Images should display cleanly with proper spacing:

{{< figure src="/imgs/Luca.jpg" width="300px" alt="Profile" >}}

## Videos

You can embed videos using the video shortcode:

{{< video src="/videos/Ensemble_Variability_and_Segmentations.mp4" width="100%" >}}

Or with options:

{{< video src="/videos/Ensemble_Variability_and_Segmentations.mp4" width="80%" loop="true" muted="true" controls="false" autoplay="true" >}}

## Horizontal Rule

---

## Spacing Control

You can add custom empty space using the `space` shortcode:

Normal paragraph spacing.

{{< space >}}

After default (medium) space.

{{< space "sm" >}}

After small space.

{{< space "lg" >}}

After large space.

{{< space "xl" >}}

After extra large space.

Available sizes: `xs` (0.5em), `sm` (1em), `md` (2em - default), `lg` (3em), `xl` (4em)

## Mixed Content

Here's a paragraph followed by a blockquote, then code:

The concept of Shibui (渋い) refers to simple, subtle, and unobtrusive beauty.

> Simplicity is the ultimate sophistication. - Leonardo da Vinci

Implementation example:

```css
blockquote {
    margin: calc(var(--spacing-base) * 1.5) 0;
    padding: 0 calc(var(--spacing-base) * 1.5);
    border-left: 2px solid var(--color-text-muted);
}
```

## Conclusion

This demo page helps visualize all the design elements in one place. It's useful for testing changes and ensuring consistency across the site.
