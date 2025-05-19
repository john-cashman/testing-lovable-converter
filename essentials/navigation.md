---
title: 'Navigation'
description: 'The navigation field in docs.json defines the pages that go in the navigation menu'
icon: 'map'
---

The navigation menu is the list of links on every website.

You will likely update `docs.json` every time you add a new page. Pages do not show up automatically.

## Navigation syntax

Our navigation syntax is recursive which means you can make nested navigation groups. You don't need to include `.mdx` in page names.

## Folders

Simply put your MDX files in folders and update the paths in `docs.json`.

For example, to have a page at `https://yoursite.com/your-folder/your-page` you would make a folder called `your-folder` containing an MDX file called `your-page.mdx`.

```json Navigation With Folder
"navigation": {
  "tabs": [
    {
      "tab": "Docs",
      "groups": [
        
      ]
    }
  ]
}
```

## Hidden Pages

MDX files not included in `docs.json` will not show up in the sidebar but are accessible through the search bar and by linking directly to them.