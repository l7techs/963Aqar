# 963Aqar website

Public website for the **963 Aqar** (963 عقار) Syrian real-estate app, in English and Arabic.

| Page | English | العربية |
| --- | --- | --- |
| Home | `/` | `/ar/` |
| Privacy Policy | `/privacy.html` | `/ar/privacy.html` |
| Terms of Service | `/terms.html` | `/ar/terms.html` |
| Contact Us | `/contact.html` | `/ar/contact.html` |
| Delete account request | `/delete-account.html` | `/ar/delete-account.html` |

Plain static HTML/CSS, served by GitHub Pages — no build step.

The Contact and Delete-account forms insert into the app's Supabase `contact_messages`
table using the public anon key (see `assets/forms.js`). Row-level security only allows
inserting new messages; admins read them in the app under **Admin → Messages**.
Deletion requests arrive with topic `account` and start with `[ACCOUNT DELETION REQUEST — Website]`.
