# Astro Starter Kit: Basics

```sh
npm create astro@latest -- --template basics
```

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
│   └── favicon.svg
├── src
│   ├── assets
│   │   └── astro.svg
│   ├── components
│   │   └── Welcome.astro
│   ├── layouts
│   │   └── Layout.astro
│   └── pages
│       └── index.astro
└── package.json
```

To learn more about the folder structure of an Astro project, refer to [our guide on project structure](https://docs.astro.build/en/basics/project-structure/).

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).

## Enquiry form

`src/components/QuoteForm.astro` posts the form to this site's `/api/website-enquiry` route (`functions/api/website-enquiry.ts`, a Cloudflare Pages Function). That route adds the private connection secret and sends the enquiry to ApexFlow CRM, where it lands in Simply Bespoke's pipeline as a New enquiry. Domestic or Commercial is added to the top of the message. Each enquiry carries a `submission_id`, so retries never create duplicates.

Cloudflare Pages settings (Settings, Variables and Secrets, Production), both shown once by Apex Admin's Connect website button on the Simply Bespoke card:

| Name | Value |
| --- | --- |
| `APEX_WEBSITE_ID` | The website connection ID |
| `APEX_WEBSITE_SECRET` | The 64 character connection secret (type: Secret) |

The old GoHighLevel webhook is no longer used by the form.
