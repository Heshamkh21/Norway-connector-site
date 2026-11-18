# Norway connector · public setup site

Public launch, connection and disconnection guidance for the locally installed
DarkVision Norway connector. This repository contains only static site files.
It contains no invoicing application, invoice data, credentials or token store.

## Enable the site once

1. Open <https://github.com/Heshamkh21/Norway-connector-site/settings/pages>.
2. Choose **Source → Deploy from a branch**.
3. Choose branch **main**, folder **/ (root)**, then **Save**.
4. Wait until GitHub displays **Your site is live at…**, then visit that address.
5. Open the Launch, Connect and Disconnect links to verify they all load.

The files are published in this repository; the website is not live until GitHub
Pages is enabled and its deployment succeeds. A GitHub-provided domain is enough;
no domain purchase is needed. Keep HTTPS enabled.

## Intuit app URL fields

Use these values after the site is live:

| Intuit field | Value |
| --- | --- |
| Host domain | `heshamkh21.github.io` |
| Launch URL | `https://heshamkh21.github.io/Norway-connector-site/launch.html` |
| Disconnect URL | `https://heshamkh21.github.io/Norway-connector-site/disconnect.html` |
| Connect/Reconnect URL | `https://heshamkh21.github.io/Norway-connector-site/connect.html` |

The repository path is case-sensitive: use **Norway-connector-site**, including
the capital **N**. If GitHub displays a different/custom site address, use its
actual host and URL prefix instead. Host domain has no protocol or path.

These are public setup pages, separate from the OAuth Redirect URI. Do not
substitute these URLs for the Production return address registered with Intuit
and saved in the local app.

## What the pages do

- **Launch:** explains how to start the installed application, then links to
  `http://localhost:5000/` on the visitor's computer.
- **Connect/reconnect:** links to the authenticated local connection settings
  and explains selecting and verifying the actual Norway company.
- **Disconnect:** explains removing saved local tokens and separately revoking
  authorization through QuickBooks. Loading the page changes no account state.

There are no credential forms, scripts, analytics or automatic calls to
localhost or accounting providers. Local links are followed only when a visitor
clicks them. Real invoice imports remain read-only; Billit remains sandbox for
separate generated tests. The public site does not serve accounting data.

The site does not yet include a company-approved EULA or privacy policy. Those
are separate from the app URL fields. These pages do not establish Intuit
Production approval; acceptance of the local-app guidance flow must be checked
in Intuit's setup/review process.

## Deployment contents

Only these site files should be deployed: `.nojekyll`, `index.html`,
`launch.html`, `connect.html`, `disconnect.html`, `site.css` and this README.
Do not copy the invoicing application's source, `.local`, `.venv`, exports or
screenshots into this public repository.
