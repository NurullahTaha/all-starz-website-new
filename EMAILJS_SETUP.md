# EmailJS Setup Guide for All Starz Fast Foods

## Quick Setup Steps

### 1. Create EmailJS Account
1. Go to [EmailJS.com](https://www.emailjs.com/)
2. Sign up for a free account
3. Verify your email address

### 2. Set Up Gmail Service
1. In your EmailJS dashboard, go to **Email Services**
2. Click **Add New Service**
3. Choose **Gmail**
4. Click **Connect Account** and sign in with `allstarskitchen2@gmail.com`
5. Copy the **Service ID** (looks like `service_xxxxxxx`)

### 3. Create Email Template
1. Go to **Email Templates**
2. Click **Create New Template**
3. Set up your template:

**Template Name:** `restaurant_review`

**Subject:** `New Review from {{from_name}} - All Starz Fast Foods`

**Content:**
```
Hello All Starz Team,

You have received a new review from your website!

Customer Details:
Name: {{from_name}}
Email: {{from_email}}

Review:
{{message}}

---
This email was automatically sent from the All Starz Fast Foods website review form.
```

4. Click **Save** and copy the **Template ID** (looks like `template_xxxxxxx`)

### 4. Get Your Public Key
1. Go to **Account** → **General**
2. Copy your **Public Key** (looks like `your_public_key_here`)

### 5. Update Your Website Code
1. Open `assets/js/script.js`
2. Find the `EMAILJS_CONFIG` section
3. Replace the placeholder values:

```javascript
const EMAILJS_CONFIG = {
    publicKey: 'your_actual_public_key_here',
    serviceId: 'service_your_service_id',
    templateId: 'template_your_template_id'
};
```

### 6. Test the Form
1. Go to your website
2. Navigate to the Location section
3. Fill out the review form
4. Submit and check `allstarskitchen2@gmail.com` for the review

## Free Tier Limits
- **200 emails/month** (free tier)
- Perfect for restaurant review forms
- No credit card required for basic usage

## Troubleshooting

### Common Issues:
1. **"EmailJS is not configured yet"** - You need to replace the placeholder values
2. **Emails not arriving** - Check spam folder, verify Gmail service is connected
3. **"Email service not available"** - EmailJS script didn't load properly

### Testing Tips:
- Use your personal email first to test
- Check browser console for error messages
- Make sure all three IDs are correctly copied

## Security Note
Your EmailJS public key can be visible in the browser - this is normal and secure. EmailJS public keys are designed to be used in client-side code.

## Support
If you need help, contact EmailJS support or check their documentation at [docs.emailjs.com](https://docs.emailjs.com) 