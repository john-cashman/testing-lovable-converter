---
title: "Custom domain"
description: "Add your own domain to any Lovable site app."
icon: "earth-europe"
---

When you create a project, Lovable makes it easy to [publish it](../features/deploy) with the click of a button.

By default, your Lovable app is accessible via a Lovable staging subdomain (e.g., `yoursite.lovable.app`). However, you can connect your site to a custom domain (e.g., `yourdomain.com`) or a subdomain (e.g., `subdomain.yourdomain.com`) that you own.

Using a custom domain enhances your brand, improves [SEO](https://docs.lovable.dev/tips-tricks/seo) discoverability, and makes your site easier to find and remember.

If you want to have a custom domain, see below.

## Using Entri

To connect a custom domain, navigate to **Project \> Settings \> Domains** in Lovable.

### Requirements

- A **paid Lovable plan** is required to connect a custom domain.
- You **must own** a domain before proceeding. If you don’t have one, you can purchase it from a domain provider such as:
  - [Namecheap](https://www.namecheap.com)
  - [GoDaddy](https://www.godaddy.com)
  - [View full list of domain providers](https://developers.entri.com/provider-list)

Lovable uses [**Entri**](https://www.entri.com/) to facilitate quick and seamless domain connections.

### Step-by-Step Guide

  
  
  
  
  </Step>
  
  
  
  </Step>
  
</Steps>

  
  
  
  
</AccordionGroup>

## Using Netlify

You can host on Netlify for free with a custom domain.

### Step-by-Step Guide

  
  
  
  
</Steps>

## Using Vercel

### Step-by-Step Guide

  
  
  
  
  
  
</Steps>

### Notes

- If you hit the 100/day deployment limit in Vercel (it builds your `dev` branch but doesn't deploy it). You can ask Lovable chat to build you vercel.json file which will force Vercel to not build development builds at all.

  ![image](https://github.com/user-attachments/assets/1b29581f-0942-432b-af30-71be43a921db)
- **Supabase Consideration**: Currently, you can only utilize one Supabase instance. So, if you make extensive SQL changes, it could potentially break production. Unfortunately, we can't yet provide specific guidelines for this scenario as it's complex. Frequently test your production environment if you make changes related to Supabase.

## Using Namecheap

### Step-by-Step Guide

  </Step>
  
  
  
  
  
  
  
  
  
</Steps>

For more information, you can check out [this site](https://custom-domain.lovable.app/).