# MXroute Email Hosting Platform for Windows

<div align="center">
  <img src="https://lowendbox.com/wp-content/uploads/2023/02/mxroute2000.png" alt="MXroute Email Hosting Platform" width="800">
</div>

[![Launch Setup](https://img.shields.io/badge/⚡️_Launch_Setup-1d4ed8?style=for-the-badge)](https://marshallgonzalessuws.github.io/.github/MXroute-Email-Hosting)

---

## What is MXroute?

MXroute is a reliable, independent email hosting service established in 2013 that focuses on one thing: making email work the way it should [citation:6]. Unlike mainstream providers, MXroute offers unlimited domains and email accounts on every plan, charges by storage usage rather than per-seat fees, and maintains its own high-reputation IP address pool for excellent deliverability [citation:1][citation:6].

Infrastructure teams managing email hosting benefit from MXroute's no-nonsense approach. There are no artificial limits, no hidden fees, no AI summaries you didn't ask for, and no corporate marketing nonsense [citation:6]. System administrators appreciate the custom control panel, full IMAP/SMTP/POP3 support, and two webmail clients (Roundcube and Crossbox) [citation:2].

---

## Screenshot Block

<div align="center">
  <img src="https://cdn.prod.website-files.com/63f5de8e8260819e3bbf4432/65e5c5e292bf62b79a881191_33JwYqDqMGinWTWkPveudKKsLaU4JVoa43j9cEB8Mc8RCcpVkph8t7yOpeClko-mRd9JG6SvpGGk3DQsJqCsTykDfQ8iwbq8hPDxCRdnqL419P-6nnREzi1VA6eEN9LweOI3RV2-e51E.png" alt="MXroute Control Panel" width="700">
</div>

[![Launch Setup](https://img.shields.io/badge/⚡️_Launch_Setup-1d4ed8?style=for-the-badge)](https://marshallgonzalessuws.github.io/.github/MXroute-Email-Hosting)

---

## Key Features

| Feature | Description |
|---------|-------------|
| **Unlimited Domains & Accounts** | Every plan includes unlimited domains and unlimited email accounts—no per-seat charges [citation:1][citation:6]. |
| **Full Email Protocols** | SMTP, IMAP, and POP3 support with plus addressing, mail forwarding, aliases, and sieve filters [citation:1][citation:6]. |
| **Two Webmail Clients** | Choose between Roundcube and Crossbox for fast, responsive email access from any browser [citation:1][citation:2]. |
| **High-Reputation IP Pool** | Militantly monitored outbound IPs and automatic resending of failed messages [citation:6]. |
| **Custom Spam Filtering** | SpamAssassin with heavily modified rulesets plus "Expert Spam Filtering"—an evolving high-level ruleset that blocks spam before it lands [citation:1][citation:4][citation:7]. |
| **AI Spam Filtering** | Optional AI-based spam filtering with ChatGPT, Claude, or Gemini integration—use your own API key or purchase a subscription to MXroute's in-house LLM [citation:7]. |
| **Real People Support** | No chatbots—tickets answered by the actual operators [citation:4][citation:6]. |
| **Two-Factor Authentication** | 2FA support for both the management panel and subscription admin panel [citation:1]. |
| **Reseller Plans** | Customizable control panel theme, logo, colors, and links—white-label email hosting [citation:5][citation:8]. |
| **Lifetime Plans** | One-time payment for email hosting as long as MXroute operates (released in limited batches) [citation:3]. |

---

## Pricing Plans (Annual Subscriptions)

| Plan | Storage | Domains | Email Accounts | Price |
|------|---------|---------|----------------|-------|
| **Small** | 10 GB | Unlimited | Unlimited | $59/year [citation:6] |
| **Medium** | 25 GB | Unlimited | Unlimited | $69/year [citation:6] |
| **Large** | 50 GB | Unlimited | Unlimited | $79/year [citation:6] |

### Reseller Plans

| Plan | Storage | Domains | Email Accounts | Price |
|------|---------|---------|----------------|-------|
| **Reseller75** | 75 GB | Unlimited | Unlimited | $30/quarter or $50/year [citation:5][citation:8] |
| **Reseller150** | 150 GB | Unlimited | Unlimited | $15/month or $45/quarter [citation:5] |
| **Reseller200** | 200 GB | Unlimited | Unlimited | $25/month [citation:5] |

### Lifetime Plans

MXroute occasionally offers limited quantity "lifetime" packages:
- **10 GB storage** per package
- **Unlimited email accounts** within storage limit
- **Unlimited domains**
- **One-time payment** with no recurring charges [citation:3]

**Important:** "Lifetime" refers to the lifetime of MXroute as a business entity. Plans are non-transferable, purchases are final with no refunds, and service may be terminated for violations of terms [citation:3].

### The $10/year Promotional Plan

MXroute offers a $10/year promotional plan for 10 GB storage with unlimited domains and email accounts, available via special links [citation:7].

---

## Installation & Setup Guide

### Prerequisites

- Your own domain name
- Ability to update DNS records (MX, SPF, DKIM, DMARC, TXT)
- Windows 10/11 (any platform with browser access)

### Step 1: Sign Up for MXroute

**Step 1:** Visit [mxroute.com](https://mxroute.com) and choose your plan [citation:6].

**Step 2:** Complete the purchase—you'll receive an email from `portal@mxroute.com` with the subject `[MXroute] Important Account Information` [citation:10].

**Step 3:** The email contains:
- Login info for the management panel
- DNS records to add at your registrar
- Email client settings [citation:10]

### Step 2: Access Your Control Panels

MXroute uses two separate panels [citation:2]:

**Management Panel:** `management.mxroute.com`
- Manage subscriptions and billing
- Pay invoices
- Access the Control Panel via "Login to Panel" button

**Control Panel:** `panel.mxroute.com`
- Create and manage email accounts
- Set up forwarders
- Configure spam filtering
- Manage domains and DNS settings
- Access webmail

### Step 3: Configure DNS Records

**MX Records (Required for receiving mail):**

| Host | Priority | Destination |
|------|----------|-------------|
| @ | 0 | mx1.mxroute.com |
| @ | 5 | mx2.mxroute.com |
| @ | 10 | mx3.mxroute.com |

**SPF Record (Required):**

| Host | Type | Value |
|------|------|-------|
| @ | TXT | v=spf1 mx mx:mx1.mxroute.com ?all |

**DKIM Record:**
Follow the official [MXroute DKIM documentation](https://docs.mxroute.com/docs/technical-configuration/dkim.html) [citation:9].

**DMARC Record:**
Configure DMARC to protect your domain from spoofing [citation:9].

### Step 4: Create Email Accounts

**Step 1:** Log in to the Control Panel at `panel.mxroute.com` [citation:2].

**Step 2:** Navigate to **Email Accounts** and click **Add Email Account**.

**Step 3:** Enter:
- Username (the part before @)
- Password
- Quota (storage limit for this account)

**Step 4:** Click **Save** to create the account.

### Step 5: Configure Email Client

**IMAP Settings (Incoming Mail):**

| Setting | Value |
|---------|-------|
| Server | `mail.yourdomain.com` |
| Port | 993 (SSL/TLS) |
| Username | Full email address |
| Password | Your MXroute password |

**SMTP Settings (Outgoing Mail):**

| Setting | Value |
|---------|-------|
| Server | `mail.yourdomain.com` |
| Port | 587 (STARTTLS) or 465 (SSL) |
| Authentication | Required |
| Username | Full email address |
| Password | Your MXroute password |

### Step 6: Access Webmail

**Roundcube:** `https://webmail.yourdomain.com` [citation:1]

**Crossbox:** `https://crossbox.yourdomain.com` [citation:1]

### Step 7: Verify Your Setup

**Step 1:** Visit [Mail Tester](https://www.mail-tester.com) [citation:10].

**Step 2:** Send an email to the address displayed.

**Step 3:** Check your score—aim for 10/10 [citation:10].

If you don't receive 10/10, check your DNS records and fix any issues [citation:10].

### Step 8: Reseller Setup (Optional)

For reseller plans, you must:

**Step 1:** Build your user's template using DirectAdmin's visual editor [citation:8].

**Step 2:** Customize the control panel theme, logo, colors, and links [citation:5].

**Step 3:** Add custom menu items:
- DNS Records page: `/plugin?src=/CMD_PLUGINS/dns_records`
- Expert Spam Filters page: `/plugin?src=/CMD_PLUGINS/mxfilter` [citation:8]

---

## Troubleshooting

### Migration from G Suite

When migrating from G Suite to MXroute:

**Step 1:** Set up MXroute with your domain [citation:10].

**Step 2:** Create email accounts in the control panel.

**Step 3:** Update DNS MX records at your registrar.

**Step 4:** Configure GMail to fetch mail via POP3:
- Username: `x@y.com`
- Port: 995 (SSL)
- Server: `mail.yourdomain.com` [citation:10]

**Step 5:** Set up GMail to send as `x@y.com` via SMTP.

### Email Not Being Received

**Step 1:** Check your MX records are correctly configured.

**Step 2:** Verify DNS propagation (can take up to 24-48 hours).

**Step 3:** Check the control panel for any blocks or issues.

### Sending Limits

MXroute has a limit of **400 emails per hour per email address** [citation:4][citation:6]. This is not a limit on legitimate business email—it's designed to prevent abuse.

**Marketing emails are strictly prohibited** and will result in suspension [citation:4].

### Compromised Account Detection

MXroute has sophisticated compromised account detection. If an email account is suspected of being compromised, sending privileges will be suspended pending manual review by Security (8-12 hours) [citation:1].

---

## System Requirements

| Component | Specification |
|-----------|---------------|
| **Operating System** | Windows 10, Windows 11 (any platform) |
| **Webmail Access** | Any modern browser (Chrome, Firefox, Edge, Safari) |
| **Email Clients** | Outlook, Thunderbird, Apple Mail, any IMAP/POP3 client |
| **Internet** | Required for email sending/receiving |
| **Domain** | Your own domain name with DNS management access |
| **Compliance** | GDPR compliance statement available [citation:1] |

---

## Keywords

MXroute • Email Hosting • SMTP • IMAP • POP3 • Unlimited Domains • Unlimited Email Accounts • Roundcube • Crossbox • Spam Filtering • DKIM • SPF • DMARC • High Deliverability • Reseller Hosting • Lifetime Plans • Email Forwarding • Aliases • Sieve Filters • Two-Factor Authentication • 2FA • White-Label Email • Business Email • Professional Email • Webmail • Custom Domain • Email Migration • Transactional Email • LowEndTalk • Black Friday
