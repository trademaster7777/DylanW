# Dylan Wallace Resume Deck - Deployment Guide

This is a professional resume deck presentation for Dylan Wallace, Co-Founder & COO of Limitless Energy Co.

## Deployment Options

### Option 1: Vercel (Recommended - Free & Easy)

1. **Install Vercel CLI** (if not already installed):
   ```bash
   npm install -g vercel
   ```

2. **Deploy to Vercel**:
   ```bash
   cd dylan_presentation_deploy
   vercel
   ```
   - Follow the prompts
   - Choose your account
   - Set project name (e.g., "dylan-resume-deck")
   - Vercel will provide a live URL

3. **Custom Domain** (if you have a Vercel account):
   - Go to your Vercel dashboard
   - Select your project
   - Go to Settings > Domains
   - Add your custom domain

### Option 2: GoDaddy Hosting

1. **Prepare Files**:
   - Download all files from the `dylan_presentation_deploy` folder
   - Zip the contents (not the folder itself)

2. **Upload to GoDaddy**:
   - Log into your GoDaddy hosting account
   - Go to cPanel or File Manager
   - Navigate to public_html (or your domain's root folder)
   - Upload and extract the zip file
   - Ensure index.html is in the root directory

3. **File Structure** should look like:
   ```
   public_html/
   ├── index.html
   ├── vercel.json (can be deleted for GoDaddy)
   ├── slides/
   │   ├── title_slide.html
   │   ├── executive_summary.html
   │   └── ... (other slide files)
   └── assets/
       ├── limitless_energy_logo.png
       └── ... (other image files)
   ```

### Option 3: GitHub Pages (Alternative)

1. Create a new GitHub repository
2. Upload all files from `dylan_presentation_deploy`
3. Go to repository Settings > Pages
4. Select source branch (usually main/master)
5. Your site will be available at: `https://yourusername.github.io/repository-name`

## Features

- **Navigation**: Use arrow keys or navigation buttons
- **Responsive Design**: Works on desktop and mobile
- **Professional Branding**: Limitless Energy Co. branding throughout
- **Confidentiality Notice**: Legal protection on all slides
- **Interactive Elements**: Smooth transitions and hover effects

## Technical Details

- Pure HTML/CSS/JavaScript (no build process required)
- Uses Tailwind CSS via CDN
- Font Awesome icons
- Chart.js for data visualizations
- Optimized for fast loading

## Support

For any deployment issues or customizations, please contact the development team.

---

**Confidentiality Notice**: This presentation contains confidential and proprietary information of Limitless Energy Co. LLC.

