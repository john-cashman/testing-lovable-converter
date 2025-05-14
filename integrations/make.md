---
title: "Integration with Make"
description: "Learn how to integrate Make with your Lovable application"
icon: "wand-sparkles"
---

## What is Make

![Make website](/images/make-hero.png)

[Make](https://www.make.com) is a powerful no-code automation platform that lets you visually build workflows across apps, APIs, and data sources.

Instead of writing backend logic, you drag, drop, and connect modules in a flowchart-style canvas. It’s ideal for:

- **Non-developers** who want automation without writing code
- **Developers** who want fast prototyping or extendability via APIs
- **Teams** looking to connect tools like Slack, Airtable, Notion, Calendly, Supabase, and more

With Make, you can:

- **Trigger actions** from your Lovable app (e.g., when a button is clicked)
- **Send and receive data** via webhooks and APIs
- **Connect with 1,500\+ tools** or custom APIs
- **Automate** tasks like emailing, AI calling, enrichment, and reminders

## Why Use Make with Lovable?

In this below tutorial, Make acts as your **AI-enabled backend**, while Lovable powers the frontend. The result: a custom CRM, built in minutes, fully automated.

This setup is ideal for:

- Non-developers needing advanced logic
- Sales teams with evolving workflows
- Fast iteration without backend overhead
- API-powered automations with real-time UI responses

## Step-by-Step tutorial

<iframe width="100%" height="315" src="https://www.youtube.com/embed/zv4vcR7VCAk?si=BgJHeEuti27cbgYt" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen />

### What we'll Build

You're going to create a CRM with three core data models:

- **Deals** (with stage-based tracking)
- **Contacts** (with inline editing)
- **Companies** (with enrichable data)

Each entity interacts with automations via Make. By the end, you’ll be able to:

- Move a deal and trigger an email
- Click a contact and start an AI sales call
- Click a company and fetch real-time data
- Secure everything via Supabase Edge Functions

### How are we going to build it

Building your own CRM can take months. With **Lovable** and **Make**, you can ship one in under an hour — and automate the entire sales workflow without writing backend code. In this step-by-step guide, you’ll learn how to build a **fully functional, AI-powered CRM**, complete with:

- Visual deal pipelines (drag-and-drop)
- Editable contact and company modals
- AI call agents using [Vapi](https://vapi.ai/)
- Company data enrichment via [Apollo.io](http://Apollo.io)
- Email workflows and security with Supabase
- Real-time automations using [Make](https://www.make.com)

    
      
      
    </Steps>
  </Step>
  
      
      
      </Step>
    </Steps>
    
  </Step>
  
      
      </Step>
    </Steps>
    
  </Step>
  
      
      
        ![Call Customer Make Pn](/images/call-customer-make.png)
      </Step>
    </Steps>
  </Step>
  
      
      </Step>
      
      
      </Step>
    </Steps>
  </Step>
  
    
  </Step>
  
  </Step>
  
      
    </Steps>
  </Step>
  
</Steps>

## Pro Tips from the Live Session

- Use **select \+ prompt** inside Lovable for precision edits
- Use **Make’s Visual Canvas** to map out flows before connecting them
- Dynamically parse unknown JSON fields into modals for UX win
- Combine Vapi \+ Apollo \+ Make for real-time AI workflows
- Use Supabase Edge Functions to mask all public API/webhook calls

## FAQ

  
  
  
  
  
  
  
</AccordionGroup>

## Resources

- [Make](https://www.make.com)
- [Vapi AI](https://vapi.ai/)
- [Apollo.io Enrichment API](https://apollo.io/docs)
- [Supabase Edge Functions](https://supabase.com/docs/guides/functions)
- Explore **Make Academy**: [academy.make.com](https://academy.make.com)