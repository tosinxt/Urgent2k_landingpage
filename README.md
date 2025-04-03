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

### Setting Up the Waitlist Form

The landing page includes a waitlist form that can collect email addresses using either Google Forms or Formspree. Here's how to set up each option:

#### Option 1: Google Forms Integration

1. Create a new Google Form at [forms.google.com](https://forms.google.com/)
2. Add an email field question
3. Click the three dots in the top right and select "Get pre-filled link"
4. Fill in any sample data and click "Get Link"
5. Copy the URL from the link
6. In `index.html`, replace the current form action URL with your Google Form URL:
   ```html
   <form id="waitlist-form" class="waitlist-form" action="YOUR_GOOGLE_FORM_URL" method="POST" target="hidden-iframe">
   ```
7. Find the entry ID for your email field by inspecting the form HTML or from the pre-filled link
8. Replace `entry.1234567890` in the email input with your actual entry ID:
   ```html
   <input type="email" name="YOUR_ENTRY_ID" placeholder="Your Email Address" required>
   ```

#### Option 2: Formspree Integration

1. Create a free account at [formspree.io](https://formspree.io/)
2. Create a new form and get your form ID
3. Uncomment the Formspree form in `index.html` and comment out the Google Forms version
4. Replace the form action with your Formspree endpoint:
   ```html
   <form id="waitlist-form" class="waitlist-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
5. Update the JavaScript in `script.js` to use the Formspree approach by uncommenting the `e.preventDefault()` line and the fetch API code

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
