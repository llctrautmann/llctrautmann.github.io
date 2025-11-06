---
title: 'Callout Demo'
date: '2025-11-06T02:00:00Z'
draft: true
tags: ['demo', 'design']
---

This page demonstrates the callout shortcode feature.

## Basic Callouts

{{< callout type="note" >}}
This is a **note** callout. Use it for general information or side notes.
{{< /callout >}}

{{< callout type="info" >}}
This is an **info** callout. Perfect for helpful information.
{{< /callout >}}

{{< callout type="tip" >}}
This is a **tip** callout. Great for sharing helpful suggestions or best practices.
{{< /callout >}}

## Warning Callouts

{{< callout type="warning" >}}
This is a **warning** callout. Use it to alert readers about potential issues.
{{< /callout >}}

{{< callout type="danger" >}}
This is a **danger** callout. Use for critical warnings or important information.
{{< /callout >}}

## Other Types

{{< callout type="success" >}}
This is a **success** callout. Great for positive outcomes or confirmations.
{{< /callout >}}

{{< callout type="question" >}}
This is a **question** callout. Use it for thought-provoking questions or discussion points.
{{< /callout >}}

## Custom Title

You can also provide a custom title:

{{< callout type="note" title="Custom Title Here" >}}
This callout has a custom title instead of the default "Note" label.
{{< /callout >}}

## With Markdown Content

Callouts support full markdown formatting:

{{< callout type="tip" >}}
You can use **bold**, *italic*, `code`, and even:

- Bullet lists
- Multiple items
- All formatted nicely

And even code blocks:

```python
def hello():
    print("Hello from a callout!")
```
{{< /callout >}}

## Usage

To use callouts in your posts, use this syntax:

```
{{</* callout type="note" */>}}
Your content here
{{</* /callout */>}}
```

Available types: `note`, `info`, `tip`, `warning`, `danger`, `success`, `question`

