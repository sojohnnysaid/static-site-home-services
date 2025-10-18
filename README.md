# Home Services Website

A clean, professional single-page website for home services (gutter cleaning, dryer vent cleaning, and water heater flush). Features flat-rate pricing and an integrated Google Form for easy service scheduling.

## Features

- 📱 Responsive design (works on mobile and desktop)
- 📞 Contact information prominently displayed
- 💰 Clear flat-rate pricing
- 📝 Modal popup for Google Form integration
- ✨ Clean, professional appearance

## Setup Instructions

### Prerequisites

- GitHub CLI installed ([install here](https://cli.github.com/))
- A Google Form created for service scheduling

### Deploying to GitHub Pages

1. **Navigate to your project directory**
   ```bash
   cd your-project-folder
   ```

2. **Make sure your HTML file is named `index.html`**
   ```bash
   # If it's named something else, rename it:
   mv yourfile.html index.html
   ```

3. **Initialize git repository**
   ```bash
   git init
   ```

4. **Add your files**
   ```bash
   git add .
   ```

5. **Commit your files**
   ```bash
   git commit -m "Initial commit - home services website"
   ```

6. **Create GitHub repository and push**
   ```bash
   # Replace 'home-services' with your desired repo name
   gh repo create home-services --public --source=. --push
   ```

7. **Enable GitHub Pages**
   ```bash
   # Option 1: Using GitHub CLI API
   gh api repos/{owner}/{repo}/pages -X POST -f source[branch]=main -f source[path]=/
   
   # Option 2: Through the web interface (easier)
   gh repo view --web
   # Then: Settings > Pages > Source: main branch > Save
   ```

8. **Your site will be live at:**
   ```
   https://yourusername.github.io/home-services/
   ```
   (GitHub Pages takes 1-2 minutes to deploy)

## Customizing the Website

### Update Contact Information

Find these lines in `index.html` and replace with your actual info:

```html
<strong>(555) 123-4567</strong>
<strong>info@homeservices.com</strong>
```

### Update Pricing

Find the price sections and adjust as needed:

```html
<div class="price">$150</div>  <!-- Gutter Cleaning -->
<div class="price">$125</div>  <!-- Dryer Vent Cleaning -->
<div class="price">$135</div>  <!-- Water Heater Flush -->
```

### Embed Your Google Form

1. Go to your Google Form
2. Click the **Send** button (top right)
3. Click the **<>** (embed HTML) icon
4. Copy the `<iframe>` code
5. In `index.html`, find this section:

```html
<!-- PASTE YOUR GOOGLE FORM EMBED CODE HERE -->
```

6. Paste your iframe code there
7. Recommended iframe settings:
   ```html
   <iframe src="YOUR_FORM_URL" 
           width="100%" 
           height="1400" 
           frameborder="0">
   </iframe>
   ```

### Making Updates

After making changes to your website:

```bash
git add .
git commit -m "Description of your changes"
git push
```

Your changes will appear on GitHub Pages within 1-2 minutes.

## Suggested Google Form Fields

Create a Google Form with these fields for best results:

- **Name** (Short answer, required)
- **Email** (Email field, required)
- **Phone Number** (Short answer, required)
- **Service Needed** (Multiple choice)
  - Gutter Cleaning ($150)
  - Dryer Vent Cleaning ($125)
  - Water Heater Flush ($135)
- **Address** (Short answer, required)
- **Preferred Date** (Date picker)
- **Preferred Time** (Multiple choice: Morning / Afternoon / Evening)
- **Additional Notes** (Paragraph, optional)

## Tips

- Test the website on mobile devices to ensure it looks good
- Update your voicemail and email to mention online booking
- Consider adding your service area/zip codes you serve
- Share the link on your Facebook page
- Keep response times quick - reply to form submissions within 24 hours

## Need Help?

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Google Forms Help](https://support.google.com/docs/topic/9055404)

## License

Feel free to modify this website for your business needs.
