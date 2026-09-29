# cPanel & WHM

Resell cPanel hosting accounts on WemX through WHM API 1. Checkout collects the domain, WHM creates the account, and customers manage it from the order page.

## Features

- Create accounts from a WHM package, with optional quota overrides
- Checkout asks for the primary domain and an optional username
- Email the customer their domain, username, password, IP, and nameservers
- One-click cPanel login for the customer, and login-as for staff
- Client tools for email, FTP, MySQL databases, addon domains, subdomains, and parked domains
- AutoSSL and a home-directory backup request
- Disk and bandwidth usage on the order page
- Suspend, unsuspend, terminate, upgrade, and password changes

## Install

Install from the WemX marketplace, or download `Cpanel.zip` from a GitHub release and place the `Cpanel` folder at `extensions/Servers/Cpanel`. Then enable **cPanel & WHM**.

Publishing a release builds `Cpanel.zip`. Unzipping it creates a folder named `Cpanel`. GitHub’s own “Source code” archive still unpacks to `server-cpanel-<tag>`. Use `Cpanel.zip`.

## Connection

Use the WHM URL without a trailing slash, for example `https://whm.example.com`, and port `2087`. Authenticate with a WHM API token from **Development → Manage API Tokens**. An access hash still works, but a token is preferred. Turn SSL verification off for a self-signed certificate.

## Packages

Pick the WHM package that sets the account limits. Disk quota, bandwidth, and the email, FTP, database, and domain caps can override that package. Leave an override empty to inherit the WHM plan.

The client panel can hide login, password changes, email, FTP, databases, domains, SSL, and backups per package.
