# Cloud Server for Small Business: What to Budget, Which Plan Is Enough, and What Gets Added to the Bill

Two numbers decide most small-business server purchases: the monthly ceiling you can live with, and what it costs to walk away. Configuration is the easy part to change later. Contracts, backup add-ons and per-IP fees are not.

Here is what a first cloud server costs in late 2026 across the plans worth comparing, which configuration suits a website versus an internal tool versus a database, and the line items that turn a €3 plan into a €7 bill.

> **Quick pick:** For a first server running a website, a small internal tool or a file share, start at 4 vCPU / 4 GB RAM / 80 GB SSD, which is SpinServers' entry KVM VPS configuration, with 8 TB of monthly transfer on a 1 Gbps port. If you need 32 GB of RAM and a terabyte of NVMe, the bare-metal tier starts at $79/mo for 4 cores, 32 GB and 1 TB NVMe, and that is the number to hold any cloud quote against. 👉 [See the current SpinServers KVM VPS configurations](https://bit.ly/Spinservers)

## The lineup: six VPS configurations and four instant dedicated servers

SpinServers sells two products a small team might buy: KVM virtual servers and bare-metal dedicated servers. The VPS range runs from 4 vCPU / 4 GB to 32 vCPU / 32 GB. Every plan includes a 1 Gbps port, one IPv4 address and one IPv6 address, with RAID-10 SSD storage on all but the largest tier.

| Plan (as listed) | vCPU / RAM | SSD | Monthly transfer | Order |
| --- | --- | --- | --- | --- |
| Simple Application Server | 4 vCPU / 4 GB | 80 GB RAID-10 | 8 TB · 1 Gbps | [Order](https://bit.ly/Spinservers) |
| Simple Application Server | 6 vCPU / 8 GB | 120 GB RAID-10 | 8 TB · 1 Gbps | [Order](https://bit.ly/Spinservers) |
| Simple Application Server | 8 vCPU / 8 GB | 160 GB RAID-10 | 10 TB · 1 Gbps | [Order](https://bit.ly/Spinservers) |
| Simple / Advanced Application Server | 12 vCPU / 12 GB | 160 GB RAID-10 | 10 TB · 1 Gbps | [Order](https://bit.ly/Spinservers) |
| Simple Application Server (Xeon) | 16 vCPU / 16 GB | 320 GB RAID-10 | 15 TB · 1 Gbps | [Order](https://bit.ly/Spinservers) |
| Advanced Application Server (Xeon) | 32 vCPU / 32 GB | 500 GB SSD | 20 TB · 1 Gbps | [Order](https://bit.ly/Spinservers) |

Pricing is quoted per configuration on the order page rather than as a single public rate card, so the table is there to show what you are choosing between. Two things are fixed across the range and both matter for a small business: you get a real 1 Gbps port with 8 TB or more of transfer included, and the IP allocation (1 IPv4 + 1 IPv6) is part of the plan rather than a separate line.

**The one limit to check before you buy:** port 25 is closed by default on every VPS. If the server will send mail, from password resets and order confirmations to a contact form, you have to open a ticket with a justification, and SpinServers reserves the right to refuse. Plan on using a transactional mail service instead of running your own SMTP.

The dedicated side has published monthly prices. These are the instant, pre-built configurations as listed in late September 2026:

| Plan | Cores / RAM | Storage | Transfer | Price |
| --- | --- | --- | --- | --- |
| Intel Xeon E3-1280 v5 (Dallas) | 4c/8t · 32 GB | 1 TB NVMe | 30 TB | $79/mo |
| Intel Xeon E3-1280 v5 (San Jose) | 4c/8t · 32 GB | 1 TB NVMe | 30 TB | $79/mo |
| Dual Intel Xeon Gold 6148 (Dallas) | 40 vCPU · 256 GB | 3.8 TB SSD | 30 TB | $235/mo |
| Dual Intel Xeon Platinum 8173M (Dallas) | 56 vCPU · 512 GB | 7.7 TB SSD | 30 TB | $390/mo |

Billing is month-to-month, with no annual contract required for these configurations. No renewal price is published for any of the four, and servers are located in the United States: Dallas, plus a California location listed in the plan name as San Jose. The uptime SLA on record is 99.99%, and support runs through ticket, phone and email.

## What gets added to the sticker price

Entry prices are real, but they are rarely the bill. Three charges do most of the damage, and they are easiest to see in UpCloud's published rate card, which is the most granular of the providers compared here.

**Backups are a percentage, not a flat fee.** UpCloud's optional backup plans add 10% of the server price for daily backups retained 24 hours, 20% for a week, 40% for a month and 60% for a year. On a €3/mo plan the day option costs €0.30, which is easy to accept. On a €28 plan it is €2.80/mo, and the year plan is €16.80/mo on top.

**Extra IP addresses are priced like a second server.** A second public IPv4 at UpCloud is €3.47/mo. That is more than its €3/mo entry plan. If you need a floating IP for failover, it is another €3.47/mo. Private IPv4, public IPv6 and the firewall cost nothing, so the meter only runs on public IPv4.

**Stopped or deleted resources can still bill.** Hetzner's cloud billing is hourly and postpaid, with a monthly cap so the bill never exceeds the plan price. Delete a server mid-month and you still owe for the hours it ran, invoiced in the next cycle. Until those outstanding charges are invoiced and paid, the account cannot be permanently deleted. Anyone planning a short trial should know that cancelling is not the same as settling.

Run the arithmetic on the cheapest credible plan and the real figure appears: €3 base, plus €0.30 for daily backups, plus €3.47 for a second IPv4, comes to €6.77/mo. That is more than double the headline.

One timing note on UpCloud's numbers specifically: pricing changes to its previous Cloud Server plans take effect 16 November 2026, so treat its current figures as pre-change and re-check before ordering. 👉 [Compare SpinServers' current VPS and dedicated pricing](https://bit.ly/Spinservers)

## How to pick a plan by workload

Match the plan to what the server has to do, not to how many people work at the company.

**A website, brochure site or low-traffic WordPress install.** The 4 vCPU / 4 GB / 80 GB plan is enough. Static pages and a cached WordPress site with a few thousand visits a day use a fraction of that. Spend the difference on backups and a staging copy instead of more cores.

**An internal tool, CRM, file share or a handful of SaaS utilities.** Move to 8 vCPU / 8 GB with 160 GB of disk. The extra disk matters more than the cores here, because file shares and document stores grow, and 80 GB fills faster than expected once you keep versions.

**A database or background job queue.** Core count and RAM both matter, and dedicated vCPUs matter more than either. Shared vCPUs on a busy host produce latency spikes that look like database problems. Hetzner's General Purpose line assigns vCPUs exclusively to one instance for this reason, and SpinServers' 16 and 32 vCPU tiers are the ones to price against it.

**Anything over 64 GB of RAM, or regulated health and financial data.** Above roughly 64 GB of RAM a dedicated server is usually both cheaper and better suited than a cloud instance, and compliance regimes in health and finance can require fully private infrastructure. SpinServers' $235/mo box with 256 GB of RAM is in this territory; so is a hybrid setup that keeps the regulated workload on dedicated hardware and the public website on a VPS.

**A note on serverless workloads.** If your load swings hard by season, hourly billing with the ability to resize without downtime is worth more than a lower base price. UpCloud bills hourly and allows scaling up or down without downtime, and Hetzner bills hourly against a monthly cap.

## How the alternatives compare on the numbers

None of these providers is universally cheaper; the differences are in what is bundled and what is restricted.

**UpCloud** lists Starter plans from €3/mo (1 GB RAM, 1 core, 10 GB storage, 250 Mbit/s) to €28/mo (16 GB RAM, 4 cores, 50 GB storage, 500 Mbit/s), on previous-generation AMD CPUs with standard-performance SSD. The Starter line carries a 99.99% SLA, while the product page advertises 99.999% for the current generation, so the number depends on which line you buy. Outbound transfer is €0/GiB.

**Hetzner** uses dedicated vCPUs, publishes a 99.9% SLA with defined credits for outages, and holds BSI C5 certification, which counts for European business. Three limits are easy to miss: official OS support is Linux only (Ubuntu, Fedora, Debian, CentOS, Rocky, AlmaLinux), Windows can be installed but is unsupported, and custom configurations such as added RAM or a larger disk are not offered. Bandwidth is not guaranteed; the 10 Gbit host connection is shared and you should expect 300–500 Mbit.

**Liquid Web** advertises cloud VPS from $11/mo with DDoS protection, firewall and automatic backups, and supports both Linux and Windows Server 2019/2022. Its Acronis disaster recovery is available only on VMware plans. That $11/mo figure comes from a page last updated in February 2024, so confirm it before you plan a budget around it.

## Who should not buy this

If you already run a dedicated server that is not maxed out, adding a cloud instance doubles your admin work for capacity you already own. Stay put.

If your site gets a few hundred visits a day and nothing on it needs root access, shared hosting at a fraction of the price will do the job, and a VPS only adds patching and monitoring to your week.

If your workload needs full physical isolation for regulatory reasons, a multi-tenant VPS is the wrong shape regardless of provider. Ask for dedicated hardware or a private environment.

And if you need Windows with vendor support, cross Hetzner off the list before you compare prices, since self-installed Windows there comes with no support.

## FAQ

**What is the real minimum a small business should budget?**
Around €3–6/mo for an unmanaged entry VPS, or $79/mo for a 32 GB dedicated box. The lower figure only holds if you skip paid backups and extra IPs; add both and the entry plan roughly doubles.

**Does the entry price include backups and a second IP?**
Not at UpCloud. Daily snapshots are included with its General Purpose, High CPU and High Memory lines, and not listed for Starter, where backups are the paid add-on priced at 10–60% of the server plan. An extra public IPv4 is €3.47/mo. For SpinServers, backup terms were not listed on the pages reviewed, so ask before ordering.

**Can I pay monthly and leave whenever I want?**
SpinServers' dedicated configurations are month-to-month, and no renewal price is published for any of them, which means the second-term price is worth asking about in writing. Hetzner bills hourly against a monthly cap, but deleted resources still generate a final invoice and an unpaid balance blocks account deletion.

**Will bandwidth cost extra?**
At UpCloud, no: outbound and inbound transfer are €0/GiB. Hetzner does not guarantee bandwidth and expects 300–500 Mbit on a shared 10 Gbit host connection. SpinServers includes 8–20 TB of monthly transfer depending on plan, on a 1 Gbps port.

**Can the server send email?**
On SpinServers, not out of the box. Port 25 is closed by default across all VPS plans, and opening it requires a support ticket with a justification; the request can be refused. Use a dedicated transactional mail provider for password resets and order confirmations.

## The decision, in one pass

A website or a light internal tool with under 20 users goes on the 4 vCPU / 4 GB plan. Add the 8 vCPU / 8 GB tier when you are storing files or running a CRM. Move to a 16 or 32 vCPU tier, or to dedicated hardware, once you are running a database that needs to stay in memory or holding more than 64 GB of RAM.

Before you pay, confirm two things: whether the price you see is the renewal price or a first-term price, and whether backups and a second IP are inside the quoted figure or added at checkout. Those two answers change the monthly total more than any CPU choice.

👉 [Check SpinServers' current plans and monthly pricing](https://bit.ly/Spinservers)
