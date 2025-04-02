# Urgent 2K - Coming Soon Landing Page

This is a responsive coming soon landing page for the Urgent 2K platform - Nigeria's premier task marketplace where users can post tasks, bid on jobs, and earn money securely.

## Features

- Modern, responsive design
- Countdown timer to launch date
- Email notification sign-up form
- Feature highlights section
- Social media links
- Mobile-friendly layout

## File Structure

```
landing-page/
├── assets/
│   ├── logo.svg
│   └── favicon.svg
├── index.html
├── styles.css
├── script.js
└── README.md
```

## Customization

### Changing the Launch Date

Edit the `script.js` file to modify the countdown timer's target date:

```javascript
// Set the launch date (currently set to 3 months from now)
const launchDate = new Date();
launchDate.setMonth(launchDate.getMonth() + 3);

// To set a specific date, use:
// const launchDate = new Date('2025-07-01T00:00:00');
```

### Updating Colors

The color scheme can be modified in the `styles.css` file by changing the CSS variables:

```css
:root {
    --primary-color: #00a651; /* Main green color */
    --secondary-color: #0056b3; /* Blue accent */
    --accent-color: #ffc107; /* Yellow accent */
    /* Other variables... */
}
```

### Social Media Links

Update the social media links in the `index.html` file:

```html
<div class="social-links">
    <a href="https://twitter.com/urgent2k" class="social-icon"><i class="fab fa-twitter"></i></a>
    <!-- Other social links... -->
</div>
```

## Email Collection

The current form is set up for demonstration purposes. To make it functional, you'll need to:

1. Create a backend API endpoint to collect email addresses
2. Update the form submission handler in `script.js` to send data to your API

## Browser Compatibility

This landing page is compatible with:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Android Chrome)

## Credits

- Font Awesome for icons
- Google Fonts (Poppins)
- Developed for Urgent 2K platform
