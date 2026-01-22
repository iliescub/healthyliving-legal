# Legal Documents Deployment Guide

This folder contains the Privacy Policy and Terms of Service for HealthyLiving app.

## Files

- `privacy-policy.html` - Complete privacy policy
- `terms-of-service.html` - Terms and conditions

## Deployment Instructions

### Option 1: GitHub Pages (FREE, Recommended)

1. **Create a GitHub Repository:**
   ```bash
   git init
   git add legal/
   git commit -m "Add legal documents"
   ```

2. **Create GitHub Repo:**
   - Go to https://github.com/new
   - Name it `healthyliving-legal` or similar
   - Make it **Public** (required for GitHub Pages)
   - Push your code:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/healthyliving-legal.git
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to repo Settings → Pages
   - Source: Deploy from a branch
   - Branch: main, folder: / (root)
   - Click Save

4. **Access URLs** (available in ~1 minute):
   - Privacy Policy: `https://YOUR_USERNAME.github.io/healthyliving-legal/legal/privacy-policy.html`
   - Terms: `https://YOUR_USERNAME.github.io/healthyliving-legal/legal/terms-of-service.html`

5. **Update App:**
   - Open `HealthyLiving/Views/PrivacyPolicyView.swift`
   - Replace `https://yourdomain.com/legal/` with your GitHub Pages URLs

---

### Option 2: Netlify (FREE, Alternative)

1. **Sign up** at https://netlify.com
2. **Drag and drop** this `legal` folder to Netlify
3. **Get your URL**: `https://your-site-name.netlify.app/`
4. **Update app** with the URLs:
   - Privacy: `https://your-site-name.netlify.app/privacy-policy.html`
   - Terms: `https://your-site-name.netlify.app/terms-of-service.html`

---

### Option 3: Your Own Domain

If you have a website (e.g., `healthyliving.app`):

1. Upload files to your web server:
   ```
   /legal/privacy-policy.html
   /legal/terms-of-service.html
   ```

2. Access at:
   - `https://healthyliving.app/legal/privacy-policy.html`
   - `https://healthyliving.app/legal/terms-of-service.html`

---

## Important Notes

### Before App Store Submission:

1. ✅ Deploy these documents to a public URL
2. ✅ Update `PrivacyPolicyView.swift` with correct URLs
3. ✅ Test that links open in Safari
4. ✅ Add Privacy Policy URL to App Store Connect
5. ✅ Add Terms of Service URL to App Store Connect

### Customization Required:

Replace placeholders in both HTML files:

- `[YOUR_EMAIL@example.com]` → Your support email
- `[YOUR_JURISDICTION]` → Your country/state (e.g., "California, USA")

### Testing:

After deployment, test the links:
1. Open app → Settings → Privacy & Security → Privacy Policy
2. Tap "View Full Privacy Policy" - should open in Safari
3. Tap "View Terms of Service" - should open in Safari
4. Verify documents display correctly

---

## App Store Connect Setup

When submitting to App Store:

1. **App Information → Privacy Policy URL:**
   - Enter: `https://YOUR_URL/legal/privacy-policy.html`

2. **App Review Information → Notes:**
   - Add: "Our Terms of Service are available at: https://YOUR_URL/legal/terms-of-service.html"

3. **App Privacy Details:**
   - Fill out privacy questionnaire
   - Reference: See `privacy-policy.html` section 2 (Data Collection)

---

## Updating Documents

If you need to update the legal documents:

1. Edit the HTML files
2. Update "Last Updated" date at the top
3. Re-deploy (GitHub Pages auto-updates on push)
4. Users will see updated version next time they open the link

---

## Legal Compliance Checklist

- [ ] Documents deployed to public URL
- [ ] URLs updated in `PrivacyPolicyView.swift`
- [ ] Tested links open in Safari
- [ ] Email address updated to your real support email
- [ ] Jurisdiction updated (if outside US)
- [ ] Privacy Policy URL added to App Store Connect
- [ ] App Privacy Questionnaire completed in App Store Connect

---

## Support

For questions about legal requirements:
- GDPR (EU): https://gdpr.eu/
- CCPA (California): https://oag.ca.gov/privacy/ccpa
- App Store Guidelines: https://developer.apple.com/app-store/review/guidelines/

**Note:** Consider consulting a lawyer for legal review before App Store submission.
