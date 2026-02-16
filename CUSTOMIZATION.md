# Portfolio Customization Guide

## Quick Start Customization

### 1. Personal Information

**Update Your Name and Title:**
- File: `index.html`
- Line: Hero section
```html
<h1 class="hero-name">Your Full Name</h1>
<h2 class="hero-title">Your Professional Title</h2>
```

**Update Typing Effect Roles:**
- File: `index.html`
- In the JavaScript section, find:
```javascript
const texts = [
    'Your Title 1',
    'Your Title 2',
    'Your Title 3',
    // Add more...
];
```

### 2. Contact Information

**Email:**
- Find all instances of `peterkimutai004@gmail.com`
- Replace with your email

**Phone:**
- Find `+254742744884`
- Replace with your phone number

**Social Media Links:**
- Update LinkedIn, GitHub, Upwork, and Fiverr URLs throughout the HTML

### 3. About Section

**Statistics:**
```html
<span class="stat-number" data-target="5">0</span> <!-- Years of Experience -->
<span class="stat-number" data-target="50">0</span> <!-- Projects -->
<span class="stat-number" data-target="100">0</span> <!-- Clients -->
```
Update the `data-target` values to your actual numbers.

**About Text:**
Update the paragraphs in the about section with your own story.

### 4. Work Experience

**For each timeline item:**
```html
<div class="timeline-date">Your Date Range</div>
<h3 class="timeline-title">Your Job Title</h3>
<h4 class="timeline-company">
    <i class="fas fa-building"></i> Company Name | Location
</h4>
<p class="timeline-description">Your description</p>
<ul class="timeline-responsibilities">
    <li>Your responsibility 1</li>
    <li>Your responsibility 2</li>
    <!-- Add more -->
</ul>
<div class="timeline-tech">
    <span>Tech 1</span>
    <span>Tech 2</span>
    <!-- Add more -->
</div>
```

### 5. Projects

**Update project information:**
```html
<div class="project-card" data-aos="fade-up">
    <div class="project-image">
        <img src="images/your-project.png" alt="Your Project">
        <div class="project-overlay">
            <div class="project-links">
                <a href="your-live-demo-url" class="project-link">
                    <i class="fas fa-external-link-alt"></i>
                </a>
                <a href="your-github-url" class="project-link">
                    <i class="fab fa-github"></i>
                </a>
            </div>
        </div>
    </div>
    <div class="project-content">
        <h3 class="project-title">Your Project Name</h3>
        <p class="project-description">Your project description</p>
        <div class="project-tech">
            <span class="tech-tag">Tech 1</span>
            <span class="tech-tag">Tech 2</span>
        </div>
    </div>
</div>
```

### 6. Skills

**Update skill levels:**
```html
<div class="skill-item">
    <div class="skill-info">
        <span class="skill-name"><i class="fab fa-react"></i> Your Skill</span>
        <span class="skill-percentage">90%</span>
    </div>
    <div class="skill-bar">
        <div class="skill-progress" data-progress="90"></div>
    </div>
</div>
```

Change the percentage value and `data-progress` attribute.

### 7. Achievements

**Add or modify achievements:**
```html
<div class="achievement-card" data-aos="zoom-in">
    <div class="achievement-icon">
        <i class="fas fa-trophy"></i>
    </div>
    <h3>Your Achievement</h3>
    <p>Achievement Issuer</p>
    <span class="achievement-year">Year</span>
</div>
```

### 8. Testimonials

**Update testimonials:**
```html
<div class="testimonial-card" data-aos="fade-up">
    <div class="testimonial-rating">
        <!-- 5 stars for 5-star rating -->
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
    </div>
    <p class="testimonial-text">
        "Your testimonial text here"
    </p>
    <div class="testimonial-author">
        <div class="author-avatar">
            <i class="fas fa-user"></i>
        </div>
        <div class="author-info">
            <h4>Client Name</h4>
            <p>Client Title/Company</p>
        </div>
    </div>
</div>
```

### 9. Resume/CV

**Update CV Link:**
- Place your resume PDF in the `images` folder
- Update the link:
```html
<a href="images/YourResume.pdf" target="_blank" class="btn btn-secondary">
    <i class="fas fa-download"></i> Download CV
</a>
```

### 10. Images

**Replace placeholder images:**
1. Add your professional photo as `me.png` in the `images` folder
2. Add project screenshots with appropriate names
3. Update image references in HTML

## Color Customization

### Change Theme Colors

Edit in `css/style.css`:

```css
:root {
    /* Change primary color (main theme color) */
    --primary-color: #6366f1;  /* Your color */
    --primary-dark: #4f46e5;   /* Darker shade */
    --primary-light: #818cf8;  /* Lighter shade */
    
    /* Change secondary color (accent) */
    --secondary-color: #ec4899;  /* Your color */
    --secondary-dark: #db2777;   /* Darker shade */
    
    /* Update gradients accordingly */
    --gradient-primary: linear-gradient(135deg, #YourColor1 0%, #YourColor2 100%);
}
```

### Popular Color Schemes

**Blue Theme (Professional):**
```css
--primary-color: #3b82f6;
--primary-dark: #2563eb;
--primary-light: #60a5fa;
```

**Purple Theme (Creative):**
```css
--primary-color: #8b5cf6;
--primary-dark: #7c3aed;
--primary-light: #a78bfa;
```

**Green Theme (Tech):**
```css
--primary-color: #10b981;
--primary-dark: #059669;
--primary-light: #34d399;
```

**Orange Theme (Energetic):**
```css
--primary-color: #f59e0b;
--primary-dark: #d97706;
--primary-light: #fbbf24;
```

## Font Customization

### Change Fonts

**In the HTML head section:**
```html
<!-- Replace with your preferred Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=YourFont:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

**In CSS:**
```css
:root {
    --font-primary: 'YourHeadingFont', sans-serif;
    --font-secondary: 'YourBodyFont', sans-serif;
}
```

## Form Integration

### EmailJS Integration

1. Sign up at [EmailJS](https://www.emailjs.com/)
2. Get your Service ID and Template ID
3. Replace the form submission code:

```javascript
// Uncomment and configure in index.html
emailjs.init('YOUR_USER_ID');

contactForm.addEventListener('submit', async (e) => {
    e.preventDefault();
    
    emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', {
        name: document.getElementById('name').value,
        email: document.getElementById('email').value,
        subject: document.getElementById('subject').value,
        message: document.getElementById('message').value
    })
    .then(() => {
        alert('Message sent successfully!');
        contactForm.reset();
    })
    .catch((error) => {
        alert('Failed to send message: ' + error);
    });
});
```

## Adding New Sections

### Basic Section Template

```html
<section id="new-section" class="section">
    <div class="container">
        <div class="section-header" data-aos="fade-up">
            <span class="section-label">Section Label</span>
            <h2 class="section-title">Section Title</h2>
            <div class="title-underline"></div>
            <p class="section-subtitle">Section description</p>
        </div>
        
        <!-- Your content here -->
        
    </div>
</section>
```

**Don't forget to:**
1. Add the section to the navigation menu
2. Add corresponding CSS if needed
3. Update the scroll animation logic if necessary

## Performance Tips

1. **Optimize Images:**
   - Use WebP format when possible
   - Compress images before uploading
   - Use appropriate sizes (no larger than needed)

2. **Minimize CSS:**
   - Remove unused styles
   - Consider minifying for production

3. **Lazy Load Images:**
   - Add `loading="lazy"` to images below the fold

## Testing Checklist

- [ ] Test on multiple browsers (Chrome, Firefox, Safari, Edge)
- [ ] Test on mobile devices
- [ ] Check all links work correctly
- [ ] Verify contact form submission
- [ ] Test navigation smooth scrolling
- [ ] Check all animations work
- [ ] Verify responsive design at different breakpoints
- [ ] Test accessibility with screen readers
- [ ] Check page load speed
- [ ] Verify all images load correctly

## Deployment

### GitHub Pages
1. Create a repository named `yourusername.github.io`
2. Push your code
3. Enable GitHub Pages in repository settings

### Netlify
1. Drag and drop your folder to Netlify
2. Or connect your GitHub repository
3. Configure build settings if needed

### Vercel
1. Import your GitHub repository
2. Deploy with one click
3. Automatic deployments on push

## Support

If you need help customizing your portfolio, feel free to:
- Check the README.md for more details
- Review the code comments in HTML, CSS, and JavaScript files
- Open an issue on GitHub
- Contact for custom development work

---

**Happy Customizing! 🎨**
