# NavCode - Learning Hub Repository

## Project Overview
NavCode is a modern, student-friendly learning hub that redirects users to external coding platforms and tracks their learning time with analytics.

## Features
- ✅ User authentication (Login/Signup)
- ✅ Admin access with code verification
- ✅ Real-time activity tracking for learning websites
- ✅ Session time logging (hours:minutes:seconds)
- ✅ Responsive design for all devices
- ✅ Role-based access (User vs Admin)
- ✅ Modern UI with smooth animations

## File Structure
```
WEBSITE/
├── INDEX.html              # Home page with login/signup links
├── login.html              # User login page
├── signup.html             # User account creation
├── admin-login.html        # Admin code verification
├── admin-dashboard.html    # Admin control panel
├── main.html               # Main user dashboard (post-login)
├── confirmation.html       # Account confirmation page
├── about.html              # About page
├── README.md               # This file
├── .gitignore              # Git ignore rules
│
├── [Images]
├── badge.png               # NavCode logo
├── WEB BG.png              # Website background
├── loa-building.jpg        # Stock image
├── istockphoto-*.jpg       # Stock images
├── TEKNO LOGO.jpg          # Brand logo
└── *.png                   # UI images
```

## User Login Flow

### For Regular Users
1. Click "SIGN UP" on home page → signup.html
2. Enter username, email, password
3. Click "Confirm" → redirected to login.html
4. Enter email and password → redirected to main.html

### For Admins
1. Click "ADMIN" button on home page → admin-login.html
2. Enter admin code: `CDKEY-325-2025_2026<ADMIN>`
3. Correct code → admin-dashboard.html
4. Wrong code → error message, try again

## Dashboard Features

### Main Dashboard (main.html)
- **Welcome Banner**: Personalized greeting with practice time
- **Website Cards**: 6 clickable learning platforms
- **Time Tracking**: Automatic session timing
- **Admin Button**: Visible only for admins
- **Role Detection**: Dynamic greeting based on login type

### Admin Dashboard (admin-dashboard.html)
- **System Stats**: Real-time analytics (0 users initially)
- **Admin Tools**: User management, analytics, settings
- **Participants View**: Switch to normal user view
- **Logout**: Return to home page

## Time Tracking System

The app tracks how long users spend on external coding websites:

1. User clicks a website card
2. Timer starts (localStorage saves start time)
3. User is redirected to external site
4. User returns to NavCode
5. Time is calculated and saved
6. Dashboard updates with new total
7. Time displays on each website card

**Data Persistence**: Uses browser localStorage (survives page refreshes)

## Browser Support
- Chrome/Brave: ✅ Full support
- Firefox: ✅ Full support
- Safari: ✅ Full support
- Edge: ✅ Full support
- Mobile browsers: ✅ Responsive design

## Technology Stack
- **HTML5**: Semantic markup
- **CSS3**: Responsive design, gradients, animations
- **JavaScript**: Vanilla (no frameworks)
- **Storage**: Browser localStorage (no database required)

## Local Storage Schema

### `navcode_user_data`
```json
{
  "role": "user|admin",
  "username": "Student Name",
  "totalScreenTime": 3600000,
  "websitesTimes": {
    "Codecademy": 1200000,
    "FreeCodeCamp": 2400000
  }
}
```

### `navcode_tracking`
```json
{
  "website": "Website Name",
  "startTime": 1676059200000
}
```

## Development Tips

### Clear User Data
To reset all user data in browser console:
```javascript
localStorage.removeItem('navcode_user_data');
localStorage.removeItem('navcode_tracking');
```

### Test Admin Access
- Admin Code: `CDKEY-325-2025_2026<ADMIN>`
- Role display: "Welcome Back Creator 👋"
- Ad Dashboard visible: Yes

### Test User Access
- Any email/password combination works for demo
- Role display: "Welcome Back [Username] 👋"
- Admin Dashboard hidden: Yes

## Responsive Breakpoints
- **Desktop**: 1200px+
- **Tablet**: 900px - 1199px
- **Mobile**: Below 900px

## Color Scheme
- **Primary**: #1da1c4 (Teal)
- **Secondary**: #16a085 (Green)
- **Background**: Linear gradient from #f0f4f8 to #e2eef8
- **Text**: #333 (Dark gray)
- **Accent**: #ff9800 (Orange for admin)

## Features by Page

### INDEX.html (Home)
- Login button
- Sign Up link
- About link
- Admin link (discreet)

### login.html
- Email input
- Password input
- Form validation
- Role set to "user" on submit

### signup.html
- Username input (8-12 chars)
- Email input
- Password input with show/hide toggle
- Role set to "user" on submit

### admin-login.html
- Admin code input (password field)
- Case-sensitive validation
- Error message display
- Role set to "admin" on correct code

### main.html (User Dashboard)
- Dynamic greeting based on role
- Time tracking display
- Website cards with time spent
- External website redirects
- Logout button
- Admin button (admins only)

### admin-dashboard.html
- Dashboard header with stats
- 6 admin feature cards
- Participants View button
- Logout button

## Notes for Future Development
- Currently no backend/database
- All data stored in browser localStorage
- Add backend API for:
  - User authentication
  - Persistent data storage
  - Time tracking analytics
  - User management
  - Security improvements

## License
© 2026 NavCode. All rights reserved.

## Contact
For issues or questions, please contact the development team.
