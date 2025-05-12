---
title: 'Development'
description: 'Preview changes locally to update your docs'
---

Follow these steps to install and run Mintlify on your operating system:

**Step 1**: Install Mintlify:

**Step 2**: Navigate to the docs directory (where the `docs.json` file is located) and execute the following command:

```bash
mintlify dev
```

A local preview of your documentation will be available at `http://localhost:3000`.

### Custom Ports

By default, Mintlify uses port 3000. You can customize the port Mintlify runs on by using the `--port` flag. To run Mintlify on port 3333, for instance, use this command:

```bash
mintlify dev --port 3333
```

If you attempt to run Mintlify on a port that's already in use, it will use the next available port:

```md
Port 3000 is already in use. Trying 3001 instead.
```

## Mintlify Versions

Please note that each CLI release is associated with a specific version of Mintlify. If your local website doesn't align with the production version, please update the CLI:

## Validating Links

The CLI can assist with validating reference links made in your documentation. To identify any broken links, use the following command:

```bash
mintlify broken-links
```

## Deployment

If the deployment is successful, you should see the following:

## Code Formatting

We suggest using extensions on your IDE to recognize and format MDX. If you're a VSCode user, consider the [MDX VSCode extension](https://marketplace.visualstudio.com/items?itemName=unifiedjs.vscode-mdx) for syntax highlighting, and [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) for code formatting.

## Troubleshooting

  
</AccordionGroup>

Curious about what changed in the CLI version? [Check out the CLI changelog.](https://www.npmjs.com/package/mintlify?activeTab=versions)