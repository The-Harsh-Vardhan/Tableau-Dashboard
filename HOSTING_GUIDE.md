# 🌐 Hosting Your Tableau Dashboard Online

This guide provides step-by-step instructions for hosting your Tableau HR Analytics Dashboard online and integrating live links with your GitHub repository.

## 🎯 **Method 1: Tableau Public (Recommended)**

### **Step 1: Prepare Your Data**
Before publishing, ensure your HR data is properly anonymized:

1. **Remove Personal Information**:
   - Replace real names with generic identifiers (Employee_001, Employee_002, etc.)
   - Remove any sensitive personal data
   - Ensure compliance with data privacy regulations

2. **Validate Data Quality**:
   - Check for any remaining sensitive information
   - Verify all calculations work correctly
   - Test all interactive elements

### **Step 2: Publish to Tableau Public**

1. **Open Tableau Desktop**
2. **Load your workbook** (`Complete_Dashboard.twbx`)
3. **Go to Server** → **Tableau Public** → **Save to Tableau Public**
4. **Create Account** (if you don't have one):
   - Visit [public.tableau.com](https://public.tableau.com)
   - Sign up with your email
   - Verify your account

5. **Configure Publishing Settings**:
   - **Workbook Name**: "HR Analytics Dashboard"
   - **Description**: Add a comprehensive description
   - **Tags**: Add relevant tags (HR, Analytics, Tableau, Dashboard)
   - **Project**: Create or select appropriate project folder

6. **Publish**:
   - Click "Save" to publish
   - Wait for upload to complete
   - Note the generated URL

### **Step 3: Example - Live Dashboard**

✅ **Successfully Published Dashboard:**
- **Live Story View**: https://public.tableau.com/views/HRDataAnalysis_17555972332030/Story?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
- **Individual Worksheets**: Available by changing the worksheet name in the URL
- **Profile**: https://public.tableau.com/app/profile/harsh.maheshwari

### **Step 4: Get Your Dashboard Links**

After publishing, you'll get several URLs:

1. **Main Dashboard URL**:
   ```
   https://public.tableau.com/views/YourDashboardName/Dashboard1
   ```

2. **Individual Worksheet URLs**:
   ```
   https://public.tableau.com/views/YourDashboardName/JobDistribution
   https://public.tableau.com/views/YourDashboardName/GenderAnalysis
   ```

3. **Embed Code** (for websites):
   ```html
   <div class='tableauPlaceholder'>
   <object class='tableauViz'>
   <!-- Tableau embed code -->
   </object>
   </div>
   ```

### **Step 4: Update Your GitHub README**

Replace the placeholder links in your README.md:

```markdown
### 📊 **Main Dashboard**
[![Live Dashboard](https://img.shields.io/badge/🔗%20Open%20Live%20Dashboard-Tableau%20Public-E97627?style=for-the-badge)](https://public.tableau.com/views/HRAnalyticsDashboard/MainDashboard)

### 📈 **Individual Worksheets**
- [📊 Job Distribution Analysis](https://public.tableau.com/views/HRAnalyticsDashboard/JobDistribution)
- [👥 Gender Demographics](https://public.tableau.com/views/HRAnalyticsDashboard/GenderAnalysis)
- [📈 Salary Analysis](https://public.tableau.com/views/HRAnalyticsDashboard/SalaryAnalysis)
- [🎯 Performance Metrics](https://public.tableau.com/views/HRAnalyticsDashboard/TopPerformers)
```

## 🎯 **Method 2: GitHub Pages with Embedded Dashboard**

### **Step 1: Create GitHub Pages Site**

1. **In your repository**, go to **Settings** → **Pages**
2. **Select source**: Deploy from a branch
3. **Choose branch**: main
4. **Folder**: / (root)
5. **Save** - your site will be available at: `https://yourusername.github.io/repository-name`

### **Step 2: Create Dashboard Page**

Create a file called `dashboard.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HR Analytics Dashboard - Live</title>
    <style>
        body { margin: 0; padding: 20px; font-family: Arial, sans-serif; }
        .dashboard-container { width: 100%; height: 800px; }
        .header { text-align: center; margin-bottom: 20px; }
    </style>
</head>
<body>
    <div class="header">
        <h1>📊 HR Analytics Dashboard</h1>
        <p>Interactive Tableau Dashboard</p>
    </div>
    
    <div class="dashboard-container">
        <!-- Tableau Public Embed Code Goes Here -->
        <div class='tableauPlaceholder' id='viz1234567890123' style='position: relative'>
            <noscript>
                <a href='#'>
                    <img alt='Dashboard' src='https://public.tableau.com/static/images/YOUR_IMAGE_URL.png' style='border: none' />
                </a>
            </noscript>
            <object class='tableauViz' style='display:none;'>
                <param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' />
                <param name='embed_code_version' value='3' />
                <param name='site_root' value='' />
                <param name='name' value='YourDashboardName&#47;Dashboard1' />
                <param name='tabs' value='no' />
                <param name='toolbar' value='yes' />
                <param name='static_image' value='https://public.tableau.com/static/images/YOUR_IMAGE_URL.png' />
                <param name='animate_transition' value='yes' />
                <param name='display_static_image' value='yes' />
                <param name='display_spinner' value='yes' />
                <param name='display_overlay' value='yes' />
                <param name='display_count' value='yes' />
                <param name='language' value='en-US' />
            </object>
        </div>
        
        <script type='text/javascript'>
            var divElement = document.getElementById('viz1234567890123');
            var vizElement = divElement.getElementsByTagName('object')[0];
            if (divElement.offsetWidth > 800) {
                vizElement.style.width='100%';
                vizElement.style.height=(divElement.offsetWidth*0.75)+'px';
            } else if (divElement.offsetWidth > 500) {
                vizElement.style.width='100%';
                vizElement.style.height=(divElement.offsetWidth*0.75)+'px';
            } else {
                vizElement.style.width='100%';
                vizElement.style.height='977px';
            }
            var scriptElement = document.createElement('script');
            scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';
            vizElement.parentNode.insertBefore(scriptElement, vizElement);
        </script>
    </div>
</body>
</html>
```

### **Step 3: Update README with GitHub Pages Link**

```markdown
### 🌐 **Live Dashboard Options**

#### **Tableau Public (Full Interactive)**
[![Tableau Public](https://img.shields.io/badge/View%20on-Tableau%20Public-E97627?style=for-the-badge&logo=tableau)](https://public.tableau.com/views/YourDashboard)

#### **GitHub Pages (Embedded)**
[![GitHub Pages](https://img.shields.io/badge/View%20on-GitHub%20Pages-181717?style=for-the-badge&logo=github)](https://yourusername.github.io/repository-name/dashboard.html)
```

## 🎯 **Method 3: Alternative Hosting Platforms**

### **Netlify (Free)**
1. **Connect** your GitHub repository to Netlify
2. **Deploy** automatically on every commit
3. **Custom domain** available
4. **URL**: `https://your-site-name.netlify.app`

### **Vercel (Free)**
1. **Import** your GitHub repository
2. **Automatic deployments**
3. **Serverless functions** support
4. **URL**: `https://your-site-name.vercel.app`

## 📋 **Best Practices for Public Dashboards**

### **Data Privacy & Security**
- ✅ **Anonymize all personal data**
- ✅ **Remove sensitive information**
- ✅ **Use sample/mock data if necessary**
- ✅ **Follow GDPR/privacy regulations**

### **Performance Optimization**
- ✅ **Optimize data extracts**
- ✅ **Limit data volume for faster loading**
- ✅ **Use appropriate aggregation levels**
- ✅ **Test on different devices**

### **User Experience**
- ✅ **Mobile-friendly design**
- ✅ **Clear navigation**
- ✅ **Intuitive filters**
- ✅ **Loading indicators**

## 🚀 **Quick Start Checklist**

- [ ] **Anonymize HR data**
- [ ] **Test dashboard functionality**
- [ ] **Create Tableau Public account**
- [ ] **Publish to Tableau Public**
- [ ] **Copy dashboard URLs**
- [ ] **Update GitHub README**
- [ ] **Test all links**
- [ ] **Optional: Set up GitHub Pages**

## 📞 **Need Help?**

If you encounter issues:

1. **Tableau Public Help**: [help.tableau.com](https://help.tableau.com/current/pro/desktop/en-us/publish_workbooks_tableaupublic.htm)
2. **GitHub Pages Guide**: [docs.github.com/pages](https://docs.github.com/en/pages)
3. **Data Privacy Guidelines**: Ensure compliance with local regulations

---

**Remember**: Once published to Tableau Public, your dashboard will be publicly accessible. Ensure all data is properly anonymized and approved for public viewing.
