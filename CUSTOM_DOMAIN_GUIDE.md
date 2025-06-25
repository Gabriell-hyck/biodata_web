# Custom Domain Setup Guide

## Quick Setup for Custom Subdomains (FREE)

### Netlify Custom Subdomain
1. Deploy to Netlify first
2. Go to Site Settings → Domain Management
3. Click "Options" → "Edit site name"
4. Choose your custom subdomain: `yourname.netlify.app`

### Vercel Custom Subdomain
1. Deploy to Vercel
2. Go to Project Settings → Domains
3. Add custom subdomain: `yourname.vercel.app`

### GitHub Pages Custom Subdomain
1. Name your repository: `yourusername.github.io`
2. Your URL will be: `https://yourusername.github.io`

## Professional Custom Domain (PAID)

### Step 1: Buy a Domain Name
**Recommended registrars:**
- Namecheap.com ($8-15/year)
- GoDaddy.com ($10-20/year)
- Google Domains ($12/year)
- Cloudflare ($8-10/year)

**Popular domain ideas:**
- yourname.com
- yourname.dev
- yourname.tech
- yourname.me
- yourcompany.com

### Step 2: Configure DNS (for each platform)

#### For Netlify:
1. In Netlify: Site Settings → Domain Management → "Add custom domain"
2. Enter your domain: `www.yourdomain.com`
3. Netlify will provide DNS records
4. In your domain registrar, add these DNS records:
   ```
   Type: CNAME
   Name: www
   Value: yoursitename.netlify.app
   
   Type: ALIAS/ANAME (or A record)
   Name: @
   Value: 75.2.60.5
   ```

#### For Vercel:
1. In Vercel: Project → Settings → Domains
2. Add your domain: `yourdomain.com`
3. Add DNS records in your registrar:
   ```
   Type: CNAME
   Name: www
   Value: cname.vercel-dns.com
   
   Type: A
   Name: @
   Value: 76.76.19.61
   ```

#### For GitHub Pages:
1. Create file `CNAME` in your repository with your domain
2. In repository: Settings → Pages → Custom domain
3. Add DNS records:
   ```
   Type: CNAME
   Name: www
   Value: yourusername.github.io
   
   Type: A
   Name: @
   Values: 185.199.108.153
           185.199.109.153
           185.199.110.153
           185.199.111.153
   ```

### Step 3: Enable HTTPS
- Netlify: Automatic (Let's Encrypt)
- Vercel: Automatic (Let's Encrypt)
- GitHub Pages: Settings → Pages → "Enforce HTTPS"

## Free Alternatives

### Using Freenom (Free domains)
1. Go to freenom.com
2. Get free domains: .tk, .ml, .ga, .cf
3. Configure DNS as above

### Using Dynamic DNS
1. NoIP.com - Free subdomains
2. DuckDNS.org - Free subdomains
3. Afraid.org - Free DNS hosting

## URL Customization Tips

### Good URL Structure:
- yourname.com
- yourproject.dev
- yourcompany.tech
- yourbrand.me

### SEO-Friendly URLs:
- Keep it short and memorable
- Use hyphens for multiple words
- Avoid numbers and special characters
- Choose relevant TLD (.com, .dev, .tech)

## Current Files Setup

I've created these files for you:
- `CNAME` - For GitHub Pages custom domain
- `_redirects` - For Netlify redirects and HTTPS enforcement

## Next Steps

1. **Choose your preferred option:**
   - Free subdomain (immediate)
   - Custom domain (professional)

2. **Deploy your site first:**
   - Upload to your chosen platform
   - Test with default URL

3. **Add custom domain:**
   - Follow platform-specific instructions above
   - Wait for DNS propagation (24-48 hours)

## Need Help?

Let me know:
- What domain name you want
- Which hosting platform you prefer
- If you need help with any specific step

Your website is ready to go live with any URL you choose!

