---
title: "Stripe & Payments"
description: "How to set up payments in your app using our Stripe integration"
icon: "credit-card"
---

![Integrate Stripe in Lovable](/images/lovable-stripe.webp)

Lovable now lets you set up Stripe entirely through **chat**.

**Chat‑driven auto‑setup (recommended)**  
   After you connect **Supabase** and save your **Stripe Secret Key** via **Add API Key**, just describe what you need:  
   - “Add three subscription tiers …”  
   - “Create a one‑time checkout for my e‑book at $29”  
   Lovable generates the checkout / portal edge functions, database tables with RLS, and UI buttons—no manual coding or webhooks unless you ask for them.

### Key Takeaways

- Use the **chat‑driven flow** for both subscriptions and one‑off payments.  
- **Never paste your Stripe Secret Key in chat.** Store it with **Add API Key**.  
- **Webhooks are opt‑in.** Lovable relies on edge‑function polling unless you request webhooks.  
- Debug in **Browser Console → Network/Errors**, **Supabase → Edge Functions → Logs**, and **Stripe Dashboard → Logs**.  
- Always test in **Stripe Test Mode**, then deploy.

## Requirements

Before integrating Stripe, ensure the following prerequisites are met:

- The project **must** be connected to Supabase. [Learn more about Supabase](https://docs.lovable.dev/integrations/supabase)
- A **Stripe account** with properly configured products.
- A working **frontend and backend**:
  - For individual product sales, ensure a shopping cart and checkout page are functional.
  - For subscriptions, set up login functionalities and different pricing tiers.

## Stripe Payment Setup (No‑Code Chat Flow)

Lovable now generates all Stripe logic for you. Once your **Stripe Secret Key** is saved with **Add API Key** and your project is **connected to Supabase**, simply tell Lovable what you need in chat—no manual Payment Links required.

  
  
</Steps>

## Advanced Integration: Webhooks & Supabase

For complex payment structures such as **subscriptions and role-based access**, Lovable recommends using **Supabase** to securely handle Stripe integration. This allows for proper webhook handling, subscription management, and role-based access control based on payment tiers.

  
    Lovable will generate the necessary SQL schema for handling payments. This includes database tables for users, subscriptions, and payments. You can review and customize these tables to fit your specific product needs before applying changes.
  </Step>
  
      
      
      
      
      </Step>
    </Steps>
  </Step>
  
      
      
      </Step>
    </Steps>
  </Step>
  
</Steps>

## Debugging & Troubleshooting

      
      
    </Steps>
  </Accordion>
  
      
      
    </Steps>
  </Accordion>
  
      
      
    </Steps>
  </Accordion>
  
      
      
    </Steps>
  </Accordion>
</AccordionGroup>