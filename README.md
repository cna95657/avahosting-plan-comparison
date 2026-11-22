# AVA Hosting: is €1.99 shared hosting enough, what does €12/year buy, and how does DMCA-ignored hosting actually work? (all plans compared)

AvaHost (also written AVA Hosting) publishes two price lists, and they buy different things. Shared hosting on cPanel starts at **€1.99/mo** for 5 GB of NVMe storage. The self-hosted app line starts at **€2.00/mo**, and the entry plan currently shows an annual offer of **€12 for the whole year**. Which one you want depends on what you need to run: a website with mail and databases belongs on the shared side, a single open-source app belongs on the Cloud Apps side.

Below are both plan tables as published, an explanation of what the €12/year deal actually covers, the three screens a deployment takes, and the cases where a Moldovan host is the wrong pick.

> **Quick picks**
> - One lightweight app (n8n, Umami, Miniflux, a wiki): Cloud Apps **Start** at €2.00/mo, or €12/year under the current annual offer.
> - A conventional website with WordPress, mail and SQL: shared **Mini** at €1.99/mo. Move to Ether or Impulse once you need more than 2 domains or 5 databases.
> - Photo and file apps (Immich, Nextcloud, PhotoPrism): their app pages start at €20/mo, which is the Pro tier.
>
> 👉 [See every AvaHost plan with today's checkout prices](https://my.ava.hosting/aff.php?aff=15562)

## Shared hosting: four plans, and no free domain on any of them

All four plans carry unmetered bandwidth, cPanel, phpMyAdmin, a free SSL certificate, daily backups, a website builder, 24/7 support and a 99.9% uptime guarantee. A free domain is not included at any tier, so budget for registering one separately.

| Plan | NVMe storage | Domains / SQL databases | Monthly price | Order |
| --- | --- | --- | --- | --- |
| Mini | 5 GB | 2 / 5 | €1.99 | [Order the Mini shared plan](https://my.ava.hosting/aff.php?aff=15562) |
| Ether | 10 GB | 4 / 15 | €3.99 | [Order the Ether shared plan](https://my.ava.hosting/aff.php?aff=15562) |
| Impulse | 20 GB | 10 / 30 | €5.99 | [Order the Impulse shared plan](https://my.ava.hosting/aff.php?aff=15562) |
| Web-elite | 100 GB | Unlimited / Unlimited | €14.99 | [Order the Web-elite shared plan](https://my.ava.hosting/aff.php?aff=15562) |

Subdomains scale with the domain allowance: 5 on Mini, 10 on Ether, 20 on Impulse, unlimited on Web-elite. The billing discount is printed under each plan at 5% for 3 months, 10% for 6 months and 15% for 12 months.

Shared hosting is the right side of the shop for PHP sites, small stores, mailboxes and anything that expects a cPanel login. One gap worth knowing before you pick the cheapest tier: the official plan page does not publish a RAM figure for shared hosting. If a plugin or theme has a memory requirement, ask support rather than assuming Mini will hold it.

## Cloud Apps: six plans, all drawing on one capacity pool

| Plan | vCPU / RAM / NVMe | Starting price | Order |
| --- | --- | --- | --- |
| Start | 1 / 1 GB / 15 GB | €2.00/mo | [Order the Start app plan](https://my.ava.hosting/aff.php?aff=15562) |
| Mini | 1 / 2 GB / 25 GB | €5.00/mo | [Order the Mini app plan](https://my.ava.hosting/aff.php?aff=15562) |
| Basic | 2 / 4 GB / 50 GB | €10.00/mo | [Order the Basic app plan](https://my.ava.hosting/aff.php?aff=15562) |
| Pro | 4 / 8 GB / 100 GB | €20.00/mo | [Order the Pro app plan](https://my.ava.hosting/aff.php?aff=15562) |
| Business | 6 / 12 GB / 150 GB | €30.00/mo | [Order the Business app plan](https://my.ava.hosting/aff.php?aff=15562) |
| Power | 8 / 16 GB / 200 GB | €40.00/mo | [Order the Power app plan](https://my.ava.hosting/aff.php?aff=15562) |

Transfer is unlimited on all six, and the Start plan page carries a "Free Trial" label. AvaHost uses two naming schemes for the same line: the marketing page on the main site calls them AVA One (€2) through AVA Ultra (€40), while the cart uses Start through Power. The cart names are the ones you'll see when you actually order.

## What the €2 plan buys, and what stays your job

Every app in the catalogue ships with automatic backups, automatic updates, one-click deployment from the catalogue, your own domain with free HTTPS, and terminal access. The €2 Start tier covers Navidrome. Most of the catalogue is listed from €5, including BookStack, Jellyfin, n8n, Ghost, WordPress, Wiki.js, Umami, Miniflux, HedgeDoc, FreeScout, Listmonk, Haven, Notifuse and Open WebUI. Pterodactyl Panel and Sure start at €10, and the storage- and CPU-hungry media apps (Immich, Nextcloud, PhotoPrism) start at €20. Each app page names the smallest plan it runs on, and the checkout preselects that plan by default.

One plan can host several apps at once, and they share the same CPU, RAM and storage. AvaHost flags this with an "Important" label on the page because the headroom is shared: one greedy app is usually the moment you move up a tier rather than adding a second plan.

The split of responsibility is stated plainly. AvaHost keeps the instance running, updated and backed up, and does not administer the software inside it. Users, content, settings and permissions are configured by you through the app's own interface. Nothing is locked in either, since these are open-source projects with their own export tools and data formats, so leaving means taking the data with you in the format the project defined.

## Deploying an app takes three screens

Buying a Cloud Apps plan is five steps: pick an app from the catalogue, read its requirements and starting price, choose a plan, choose a billing cycle, then check out with an optional promo code, an account, the terms of service and payment.

Deployment is shorter. The dashboard runs **App → Size it → Review**. In Size it, you select the capacity pool that came from your plan, choose a location (leaving "Best available" is fine), then assign CPU cores, RAM and disk with usage bars showing what remains for other apps. You give the instance a name and claim a subdomain, which becomes something like `my-app.avahost.app`. For n8n the deployment screen shows 1 vCPU, 2 GB RAM and 5 GB of disk; AvaHost labels those as example values, so check the minimums on the app page instead of copying them.

There is no second payment at this stage, because the deployment draws on capacity you already bought. When the install finishes you get an email with the app URL and app-specific setup instructions. n8n expects the first visitor to create the owner account with an email, first name, last name and password, so open the app soon after the email arrives to lock down access.

Afterwards the dashboard shows status, address, assigned capacity and current usage, with stop, restart and delete controls, plus tabs for credentials, console, logs and files, snapshots, environment variables, domains and access control. Each app also gets setup guides.

👉 [Start a deployment on the €2 Start plan](https://my.ava.hosting/aff.php?aff=15562)

## The real cost: €2 a month against €12 a year

Start at €2/mo comes to €24 across twelve months. The annual offer displayed on the plan is €12 for the year, so annual billing halves the bill. AvaHost's own note says prices and discounts can change and that the amount in your configuration summary is the price of your order, so treat €12 as the currently displayed offer rather than a permanent rate.

Shared hosting discounts work the same way. Mini at €1.99/mo is €23.88 over a year before any discount, and the 15% annual discount brings it to roughly €20.30. Those figures are my arithmetic on the published monthly rates; the checkout shows the number you'll actually pay.

Renewal pricing is the open question. It isn't published on the plan pages, one review-tracking site lists the renewal price as "not published", and a 2026 third-party review mentions user complaints about renewing at a higher price than the first term. Confirm the renewal terms at checkout before you commit to a long billing cycle.

👉 [Compare the Start plan's monthly and annual pricing](https://my.ava.hosting/aff.php?aff=15562)

## Who AvaHost suits, and who should host elsewhere

The reason most people search for this brand is the content policy. AvaHost operates from a data centre in Chișinău, Moldova, and markets a DMCA-ignored option. In practice that means a takedown notice doesn't trigger automatic removal; the complaint gets looked at, and Moldovan jurisdiction sets the boundaries rather than US copyright law. It does not mean anything goes. The terms still prohibit universally illegal material such as child sexual abuse content and terrorism, and a host reviewing complaints can still suspend an account.

That positioning attracts a specific audience: adult publishers dealing with repeat claims, file-sharing and streaming projects with user-generated content, forums where copyright trolls target posts, and anyone who wants a non-US jurisdiction on principle. Crypto payment is part of the appeal, and a third-party review lists cards, PayPal and a range of coins processed through Cryptomus. European visitors get decent latency from Moldova; US West Coast visitors get noticeably more.

The same third-party review flags policy details worth reading before you pay. Registration collects name, address and phone number, and the refund policy reportedly reserves the right to request a passport through the payment gateway. The same review reports traffic logs kept for 12 months and a ban on Tor exit relays. If identity handling or logging decides where you host, read the terms and refund policy first.

Skip AvaHost if you need HIPAA or PCI-DSS certification, a phone support line, or a fully managed WordPress setup. Support runs on live chat, tickets and email; a third-party review describes English coverage as around the clock, with Russian and Ukrainian during business hours.

The shop also lists VPS and dedicated server lines, which this page leaves unpriced because their current rates weren't on the official pages used here. Third-party roundups put VPS plans somewhere between €5 and €40/mo, so check the store before you budget.

## FAQ

**Which plan does the €12/year price apply to?**
Start, the €2/mo entry tier, on annual billing. It is a displayed offer, and AvaHost says prices and discounts change, so confirm the total on the checkout screen.

**Can I run several apps on one plan?**
Yes. Apps share the plan's CPU, RAM and storage, and AvaHost marks this as important because a heavy app can consume the headroom the others need.

**Do I have to manage the server?**
No. The OS, certificates, updates and backups are handled for you. You do manage the application itself: its users, content, settings and permissions.

**How long until the app is live?**
A few minutes in most cases. The exact time depends on the application, and you get an email with the URL and setup instructions once it's ready.

**Can I get a refund?**
Third-party reviews report a 30-day money-back window for first-time hosting accounts, with discounted orders excluded and fees on crypto refunds. Check the refund policy on the site before paying.

## Before you order

Use the plan that matches the job rather than the one with the best spec sheet. A single light app runs fine on Start, monthly if you're unsure and annual if you're staying. Two or three apps, or one that's memory-hungry, puts you on Mini or Basic. Immich, Nextcloud and PhotoPrism start at Pro for a reason. A conventional website with mail and databases belongs on shared hosting, where Mini covers a first site and Ether or Impulse cover growth.

Two things to confirm at checkout: the total for the billing cycle you selected, since the offer on the page and the invoice can differ, and the minimum resources listed on the app page before you allocate CPU and RAM.

👉 [Pick a plan and open an AvaHost account](https://my.ava.hosting/aff.php?aff=15562)
