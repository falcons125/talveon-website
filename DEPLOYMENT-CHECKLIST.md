# Talveon.com - Deployment Checklist

## Pre-Deployment

- [ ] Review all website content for accuracy
- [ ] Test all links work correctly
- [ ] Verify contact email (info@talveon.com) is set up in Google Workspace
- [ ] Check website on mobile device preview
- [ ] Ensure all images are optimized (if you add any)

## Netlify Deployment

- [ ] Sign up for Netlify account at https://netlify.com
- [ ] Deploy website using drag & drop method
- [ ] Verify site works at temporary .netlify.app URL
- [ ] Test contact form submission

## Domain Configuration

### Option A: Netlify DNS (Recommended)
- [ ] In Netlify: Set up Netlify DNS
- [ ] Copy Netlify nameservers (4 DNS addresses)
- [ ] In Porkbun: Update nameservers to Netlify's
- [ ] Add Google Workspace MX records in Netlify DNS:
  - [ ] MX Priority 1: ASPMX.L.GOOGLE.COM
  - [ ] MX Priority 5: ALT1.ASPMX.L.GOOGLE.COM
  - [ ] MX Priority 5: ALT2.ASPMX.L.GOOGLE.COM
  - [ ] MX Priority 10: ALT3.ASPMX.L.GOOGLE.COM
  - [ ] MX Priority 10: ALT4.ASPMX.L.GOOGLE.COM
- [ ] Add Google Workspace TXT records (SPF, DKIM, verification)

### Option B: Porkbun DNS
- [ ] Get A record IP from Netlify (usually 75.2.60.5)
- [ ] Get CNAME record from Netlify
- [ ] In Porkbun DNS: Add A record for @ pointing to Netlify IP
- [ ] In Porkbun DNS: Add CNAME for www pointing to your-site.netlify.app
- [ ] Verify Google Workspace MX records are still in place

## SSL/HTTPS

- [ ] Wait for DNS propagation (can take up to 48 hours)
- [ ] In Netlify: Verify DNS configuration
- [ ] In Netlify: Provision SSL certificate
- [ ] Enable "Force HTTPS" option
- [ ] Test https://talveon.com loads correctly
- [ ] Test https://www.talveon.com redirects to main domain

## Email Verification

- [ ] Send test email FROM your @talveon.com address
- [ ] Send test email TO your @talveon.com address
- [ ] Verify both emails work correctly
- [ ] Check spam folder if emails don't arrive

## Post-Launch

- [ ] Submit site to Google Search Console
- [ ] Submit sitemap.xml to Google Search Console
- [ ] Set up Google Analytics (optional)
- [ ] Test contact form and verify you receive submissions
- [ ] Check website on multiple browsers (Chrome, Firefox, Safari, Edge)
- [ ] Test website on mobile phone
- [ ] Set up Netlify form notifications (email alerts for new submissions)

## Monitoring

- [ ] Bookmark your Netlify dashboard
- [ ] Set up uptime monitoring (UptimeRobot - free tier available)
- [ ] Save all login credentials securely
- [ ] Document any custom configurations

## Optional Enhancements

- [ ] Add favicon (small icon in browser tab)
- [ ] Add Open Graph tags for social media sharing
- [ ] Create additional pages as needed
- [ ] Add blog section
- [ ] Integrate with CRM or email marketing tool
- [ ] Set up automated backups

## Notes

DNS Propagation Time: 5 minutes to 48 hours (typically 1-4 hours)
Check DNS status: https://dnschecker.org

## Contact Information

- Netlify Support: https://answers.netlify.com
- Porkbun Support: https://porkbun.com/support  
- Google Workspace Support: https://support.google.com/a

---

**Current Status:**

Date Started: _______________
Deployed to Netlify: _______________
DNS Updated: _______________
Site Live: _______________
