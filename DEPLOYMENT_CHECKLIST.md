# Deployment Checklist - Hardin AI Website Updates

## Pre-Deployment

- [x] Create industry landing pages (Healthcare, Finance, E-commerce, Education)
- [x] Update homepage with industry cards and testimonials
- [x] Improve SEO meta tags and structured data
- [x] Update sitemap.xml with new pages
- [x] Test all internal links
- [x] Verify responsive design on mobile

## Deployment Steps

### 1. Upload Files to Server
```bash
# SSH into AWS Lightsail server
ssh -i your-key.pem ubuntu@35.177.54.44

# Navigate to website directory
cd /var/www/hardinai

# Pull latest changes from GitHub (if using Git)
git pull origin main

# OR manually upload files:
# - /industries/healthcare.html
# - /industries/finance.html
# - /industries/ecommerce.html
# - /industries/education.html
# - /index.html (updated)
# - /sitemap.xml (updated)
```

### 2. Set Correct Permissions
```bash
# Ensure correct ownership
sudo chown -R www-data:www-data /var/www/hardinai

# Set correct permissions
sudo chmod -R 755 /var/www/hardinai
```

### 3. Test Website
- [ ] Visit https://hardinai.co.uk and verify homepage loads
- [ ] Test all 4 new industry pages:
  - [ ] https://hardinai.co.uk/industries/healthcare.html
  - [ ] https://hardinai.co.uk/industries/finance.html
  - [ ] https://hardinai.co.uk/industries/ecommerce.html
  - [ ] https://hardinai.co.uk/industries/education.html
- [ ] Verify all internal links work
- [ ] Check testimonials section displays correctly
- [ ] Test on mobile devices
- [ ] Verify contact email links work

### 4. SEO Submission

#### Google Search Console
- [ ] Log in to Google Search Console
- [ ] Submit updated sitemap: https://hardinai.co.uk/sitemap.xml
- [ ] Request indexing for new pages:
  - [ ] /industries/healthcare.html
  - [ ] /industries/finance.html
  - [ ] /industries/ecommerce.html
  - [ ] /industries/education.html

#### Bing Webmaster Tools
- [ ] Log in to Bing Webmaster Tools
- [ ] Submit updated sitemap
- [ ] Request indexing for new pages

### 5. Analytics Setup
- [ ] Verify Google Analytics tracking on all new pages
- [ ] Set up conversion goals for industry page contact forms
- [ ] Create custom segments for each industry vertical

### 6. Social Media Updates
- [ ] Update LinkedIn company page with new industry focus
- [ ] Post about new industry-specific services
- [ ] Share case studies and testimonials

### 7. Business Directories
- [ ] Submit to UK business directories
- [ ] Update Google Business Profile
- [ ] List on industry-specific directories:
  - [ ] Healthcare directories
  - [ ] Finance/fintech directories
  - [ ] E-commerce directories
  - [ ] Education directories

## Post-Deployment Monitoring

### Week 1
- [ ] Monitor Google Search Console for crawl errors
- [ ] Check Google Analytics for traffic to new pages
- [ ] Monitor server logs for 404 errors
- [ ] Test all pages on different browsers (Chrome, Firefox, Safari, Edge)

### Week 2-4
- [ ] Track keyword rankings for target terms:
  - "healthcare AI UK"
  - "NHS AI solutions"
  - "finance AI banking UK"
  - "ecommerce AI retail UK"
  - "education AI training UK"
- [ ] Monitor conversion rates per industry page
- [ ] Analyze user behavior (time on page, bounce rate)
- [ ] Collect feedback from visitors

### Month 2-3
- [ ] Review SEO performance
- [ ] Analyze lead quality per industry
- [ ] A/B test CTAs and page layouts
- [ ] Create additional content based on performance data

## Rollback Plan

If issues occur:
```bash
# Restore previous version
cd /var/www/hardinai
git checkout HEAD~1

# Or restore from backup
sudo cp -r /var/www/hardinai-backup/* /var/www/hardinai/

# Restart Nginx
sudo systemctl restart nginx
```

## Success Metrics

### Traffic Goals (3 months)
- [ ] 50% increase in organic search traffic
- [ ] 100+ visits to industry pages per month
- [ ] 20% reduction in bounce rate

### Lead Generation Goals (3 months)
- [ ] 10+ qualified leads from industry pages
- [ ] 5+ demo requests from target companies
- [ ] 2+ signed contracts from target industries

### SEO Goals (3 months)
- [ ] Rank in top 10 for "healthcare AI UK"
- [ ] Rank in top 10 for "finance AI UK"
- [ ] Rank in top 10 for "ecommerce AI UK"
- [ ] Rank in top 10 for "education AI UK"

## Notes

- All pages are GDPR-compliant
- Healthcare page emphasizes NHS compliance
- Finance page emphasizes FCA compliance
- All pages include clear CTAs and contact information
- Testimonials add social proof and credibility
- Structured data improves search engine understanding

## Contact for Issues

**Technical Issues:** info@hardinai.co.uk  
**Server Access:** AWS Lightsail (35.177.54.44)  
**DNS:** Managed at domain registrar

---

**Deployment Date:** _____________  
**Deployed By:** _____________  
**Verified By:** _____________
