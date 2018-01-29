Nayara Rodríguez Rodríguez

# How to exclude concrete traffic sources from Google Analytics metrics

### First of all, what is referral traffic?

Referral traffic is the segment of traffic that arrives on a website/app through another source, like through a link on another domain or on social networks. Analytics automatically recognizes where traffic was immediately before arriving on a site, and displays the domain names of these sites as the referral traffic sources in its reports.

### Ok, why did you need this?

Nícoli's payment methods force the users to go outside the website and coming back after paying, so Google Analytics thinks PayPal and Redsys are important traffic sources... But this is not true. So they asked us to fix this.

### Oh I see... So how can I exclude these domains from my Google Analytics traffic sources report?

By using: **Google Analytics Referral Exclusion List**!

1. Sign in to your Analytics account.
2. Click Admin (yes, sorry but you can't do this unless you are a Google Analytics account administrator).
3. In the ACCOUNT column, use the dropdown to select the Analytics account that contains the property you want to work with.
4. In the PROPERTY column, use the dropdown to select a property. (yes, this is list is at property level!)
5. Click Tracking Info.
6. Click Referral Exclusion List.
7. To add a domain, click +ADD REFERRAL EXCLUSION.
8. Enter the Domain name. (Google Analytics has matching, so you'll be excluding subdomains too!)
9. Click Create to save.
10. Feel happy and satisfied for what you did!
