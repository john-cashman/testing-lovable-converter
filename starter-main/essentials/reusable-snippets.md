---
title: Reusable Snippets
description: Reusable, custom snippets to keep content in sync
icon: 'recycle'
---

### Default export

1. Add content to your snippet file that you want to re-use across multiple
   locations. Optionally, you can add variables that can be filled in via props
   when you import the snippet.

```mdx snippets/my-snippet.mdx
Hello world! This is my content I want to reuse across pages. My keyword of the
day is .
```

2. Import the snippet into your destination file.

```mdx destination-file.mdx
---
title: My title
description: My Description
---

## Header

Lorem impsum dolor sit amet.

2. Import the snippet into your destination file and pass in the props

```mdx destination-file.mdx
---
title: My title
description: My Description
---

Lorem ipsum dolor sit amet.

```