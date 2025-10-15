---
title: "Table of Contents and Details"
draft: false
toc: true
tocBorder: true
---

## Table of Contents

The table of contents is a feature that allows you to display a list of headings
in a post, making it easier for readers to navigate through the content.

The table of contents is automatically generated from the headings in the post.

### Enabling the Table of Contents

To enable the table of contents for a post, add the following to the post's
front matter:

```toml
toc = true
```

You can also add a border by setting:

```toml
tocBorder = true
```

## Details Shortcode

The `details` shortcode allows you to create collapsible sections in your
content. This is useful for hiding content that is not immediately relevant,
such as code snippets, examples, or additional information.

### Usage

To use the `details` shortcode, wrap the content you want to hide in a `details`
block:

{{< details summary="Click to expand" >}}
This is the content that will be hidden until the user clicks on the summary text.
You can include any type of content here, such as text, code blocks, or even
other shortcodes.
{{< /details >}}

To learn how to use it, you can see this file at
`themes/unstyled/content/toc-and-details.md`
