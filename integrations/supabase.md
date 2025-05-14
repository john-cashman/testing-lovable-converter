---
title: "Supabase Integration"
description: "Integrate a full-featured backend into your Lovable application with Supabase."
icon: "database"
---

Lovable’s **native** [Supabase](https://supabase.com/) **integration** lets you manage both your front-end UI and your back-end database through a single, easy-to-use chat interface. In other words, you can design your app’s screens _and_ set up a cloud PostgreSQL database without leaving Lovable. This unified approach makes powerful app development accessible to everyone – non‑technical users can rely on Lovable’s guidance, while experienced developers can tap into advanced Supabase features as needed.

## Overview

<iframe width="100%" height="315" src="https://www.youtube.com/embed/-sSOyO0FiPE?si=WljVA-E0YU4LObMY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen />

Supabase is an open-source alternative to Firebase, providing a hosted PostgreSQL database with real-time capabilities, user authentication, file storage, and serverless functions. By connecting Supabase to your Lovable app, you instantly gain a production-ready backend without writing any boilerplate code or manually configuring servers. Supabase’s intuitive web dashboard makes it easy to manage your data and users, and its robust SQL foundation means you retain the full power and scalability of a PostgreSQL database.

### **Key features unlocked by Supabase integration:**

- **Database (PostgreSQL)** – Store and query your app data with full SQL support. Lovable can automatically generate the necessary tables and schema based on your prompts.
- **User Authentication** – Securely manage user sign-ups, logins, and access control. Lovable can add pre-built authentication flows (email/password, etc.) to your app with a simple prompt.
- **File Storage** – Upload and serve images or other files via Supabase Storage. Great for user profile photos, uploads, or any static media your app needs to handle.
- **Real-time Updates** – Supabase can stream live data changes to your app. This enables features like live chat, activity feeds, or collaborative dashboards that update instantly for all users.
- **Edge Functions (Serverless)** – Run custom backend logic (in JavaScript/TypeScript) on Supabase’s infrastructure. Lovable will create and deploy these functions for tasks like sending emails, processing payments, or integrating with external APIs.

### **Why use Lovable’s Supabase integration?**

With Lovable, you don’t have to juggle separate tools for front-end design and back-end setup. By simply conversing with Lovable’s AI, you can build your UI _and_ have the underlying database and server functions created for you automatically. This means faster development and fewer integration headaches. For example, if you prompt Lovable with “Add a user feedback form and save responses to the database,” Lovable will generate the form UI **and** set up a Supabase table to store the feedback – all in one go. This seamless end-to-end generation is Lovable’s unique strength, empowering beginners to build complex apps and allowing power users to move faster.

## Getting Started: Connecting Supabase to Lovable

Connecting a Supabase backend to your Lovable project is straightforward. You’ll need a Supabase account (free tier is fine) and a Lovable project ready. If you don’t have a Supabase account yet, you can sign up at the Supabase website – no credit card required for the free tier.

<iframe width="100%" height="315" src="https://www.youtube.com/embed/V_2aZCjrTJo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen />

  
  
      
      
    </Steps>
    
  </Step>
</Steps>

## Adding User Authentication

One of the first things you’ll likely want is user authentication (so people can sign up and log into your app). Lovable’s Supabase integration makes this trivial to set up via chat.

<iframe width="100%" height="315" src="https://www.youtube.com/embed/LHpMUj-Jf_k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen />

### Email and Password (Basic Setup)

Once your project is connected to Supabase, Lovable can generate authentication pages for you. For example, you can simply prompt: **“Add login”**. This will typically create a basic login page (and related signup flow) in your app, wired up to Supabase’s authentication system.

After Lovable adds the login UI, you have a couple of ways to create users for testing:

- **Via your app’s signup form:** Use the newly added interface in your app to register a user (this will communicate with Supabase to create the account).
- **Via Supabase Dashboard:** Go to your Supabase project’s dashboard, navigate to **Authentication \> Users**, and manually add a new user (email and password). This is handy to set up a test account quickly.

Lovable will have already configured your Lovable app to recognize authenticated users (for example, gating certain pages to logged-in users only, if appropriate). You can further customize the look and feel of the login/signup pages using Lovable’s editor or prompts. Supabase Integration 2.0 even allows adding extra fields to your signup form or styling the form to match your brand.

### Social Logins (e.g. Google)

<iframe width="100%" height="315" src="https://www.youtube.com/embed/W6-_0-Eekio?si=8WkxiJn0oe4wfSbe" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen />

Supabase supports OAuth logins like Google, GitHub, Twitter, and more. You can integrate these into your Lovable app as well:

1. **Enable the provider in Supabase:** In your Supabase dashboard, navigate to **Authentication \> Providers**. You’ll see a list of external login providers. Toggle on **Google** (for example) and follow the instructions to provide the required OAuth Client ID and Secret from Google. _(Supabase will guide you on how to obtain these credentials from Google’s developer console.)_ Save the settings – your Supabase project now knows how to handle Google logins.
2. **Update your Lovable app’s UI:** Next, you can prompt Lovable to add a social login option. For instance: **“Add a ‘Sign in with Google’ button to the login page.”** Lovable will modify the authentication page, adding a Google sign-in button and the necessary code to initiate the OAuth flow via Supabase.

Once this is done, users of your app will be able to click “Sign in with Google”, be redirected to Google for authentication, and then return to your app as logged-in users. You can enable other providers (GitHub, Facebook, etc.) in a similar way – just remember to configure each in Supabase and then adjust your Lovable UI accordingly.

## Managing Data with Supabase

Beyond authentication, the core of most apps is reading and writing data. With Lovable and Supabase, you can create database tables and connect them to your UI without leaving the chat prompt.

<iframe width="100%" height="315" src="https://www.youtube.com/embed/V5LdDEuCli4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen />

### Creating Database Tables via Lovable

After connecting Supabase, whenever you need to store data persistently, you can instruct Lovable and it will coordinate the database setup for you. The process typically looks like this:

  
  
  
</Steps>

That’s it\\! You didn’t have to manually design a database schema or write any backend code – Lovable and Supabase handled it from your description. You can repeat this process for any new data feature (blog posts, comments, products, etc.).

For example, if you want users to be able to post articles in your app, you could prompt: **“Allow users to create posts with a title and content, and store these in the database.”** Lovable would generate a `posts` table (with fields for title, content, author, timestamps, etc.), give you the SQL to add it to Supabase, and then wire up the front-end forms and pages to that table.

### File Storage (Images & Media)

When your Lovable app needs to handle file uploads (for example, user profile pictures, attachments, or any media), Supabase integration has you covered. Supabase includes a **Storage** service for hosting files (images, videos, PDFs, etc.) conveniently alongside your database.

If you add an **Upload** component or an image upload feature in your Lovable app, Lovable will utilize Supabase Storage behind the scenes. Uploaded files will be stored in a storage bucket within your Supabase project, and you’ll get a URL or reference to use for displaying or downloading the file later.

By default, Supabase’s free tier allows files up to **50MB** each to be uploaded. This is plenty for most images or short videos. If your app needs to handle larger files, Supabase’s paid plans support bigger uploads (including **resumable uploads** for very large files). You can organize files into folders (buckets) and manage access permissions via the Supabase dashboard as needed.

## Storing Secrets (API Keys & Config)

Many applications need to use secret keys or API credentials for third-party services (for example, Stripe API keys for payments or OpenAI keys for AI features). With Supabase connected, Lovable provides a secure way to store and use these secrets.

You can add secret keys to your Lovable project in two ways:

1. **Project Settings UI:** In Lovable, go to your project’s settings and find the **Secrets** section. Here you can add keys (name and value).
2. **Via Prompt:** You can ask Lovable something like “Show me the secrets form” in the chat, and it will present a UI to input secret values.

Under the hood, Lovable stores these secrets in **Supabase’s Edge Function secret manager** for your project. They are encrypted and kept safe on the backend. When you deploy Edge Functions (see next section), those functions can retrieve these secrets to interact with external services.

## Backend Logic with Edge Functions

<iframe width="100%" height="315" src="https://www.youtube.com/embed/p_hKIDlxXp0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen />

Sometimes your app needs custom backend logic beyond basic data CRUD (Create, Read, Update, Delete). **Supabase Edge Functions** are serverless functions (similar to AWS Lambda) that let you run code on the backend triggered by events or requests. Lovable’s integration means you can define desired backend behavior in plain language, and Lovable will write and deploy the necessary Edge Function code to Supabase for you.

Typical use cases for Edge Functions in Lovable include:

- **Using AI services:** e.g. processing some input with OpenAI or Anthropic APIs (with the API key stored as a secret as described above).
- **Sending emails or notifications:** e.g. sending a welcome email when a user signs up, via an email API like Resend.
- **Processing payments:** e.g. creating a checkout session or fulfilling an order using Stripe’s API.
- **Scheduled tasks:** e.g. performing a cleanup or summary job every hour/day (Supabase Edge Functions can be triggered on a schedule).
- **Complex computations or third-party integrations:** any code that you don’t want to run on the client-side can be done in an Edge Function.

To add a backend function, simply describe what you need in the Lovable chat. For example: _“When a user submits the feedback form, analyze the text using OpenAI and store a sentiment score.”_ Lovable will generate the code for this logic as a Supabase Edge Function (in this case, calling the OpenAI API) and deploy it to your Supabase project. It will also update your Lovable app to call this function at the right time (e.g., on form submission) and handle the response.

You can find and monitor your Edge Functions in the Supabase dashboard under **Functions**. Each function will have logs that show recent executions and any output or errors. Lovable’s Supabase Integration 2.0 improves this experience by automatically reading those logs when something goes wrong – if your function errors out, Lovable will surface the error message in the chat to help you troubleshoot. Of course, you can always check the Supabase logs yourself for more details or for peace of mind.

### FAQ

  
  
  
  
  
  
  
  
  
  
  
</AccordionGroup>