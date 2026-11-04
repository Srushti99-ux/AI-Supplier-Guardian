# AI Supplier Guardian

Portfolio edition by Srushti Raj Beerelli.

AI Supplier Guardian helps buyers review delivery delays and price changes in supplier emails. This repository contains the React dashboard and Supabase schema. The email workflow runs separately in n8n.

## Verified workflow test

A sample Gmail message for PO-4421 reported a 30-day delivery delay and a price increase from $4,200 to $4,500. The n8n workflow retrieved the message, used Gemini to extract the order details and assess the risk, then parsed the result. Gemini rated it **High** and recommended contacting the supplier and evaluating backups.

I configured Supabase and tested the Gmail-to-Gemini workflow. The automatic write from n8n to the dashboard is pending.

## Run locally

1. Clone `https://github.com/Srushti99-ux/AI-Supplier-Guardian.git` and run `npm ci` in the repository.
2. Copy `.env.example` to `.env`. Set `VITE_SUPABASE_URL` and `VITE_SUPABASE_ANON_KEY` to your project's URL and publishable or legacy anon key.
3. For a fresh Supabase project, run `supabase/schema.sql` once in the SQL Editor.
4. Run `npm run dev`, open the localhost URL shown in the terminal, and sign up or log in.

[Portfolio walkthrough](https://srushti-analytics-portfolio.thoughtfulturnip.chatgpt.site)

## Credits and license

Based on [AI Supply Guardian](https://github.com/abdullahxyz85/AI-Supply-Guardian). The upstream README identifies the project license as MIT.
