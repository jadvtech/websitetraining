# JADV Professional Training Institute - IT Training Website

A modern, responsive React website for JADV Professional Training Institute built with React, Tailwind CSS v4, and shadcn/ui components.

## Features

- Modern, minimalistic UI with clean design
- Dark/Light theme toggle
- Fully responsive (mobile-first design)
- 5 main pages: Home, Courses, Course Details, About, Contact
- Smooth animations and transitions
- Form validation on contact page
- Google Sheets integration for enrollment data
- SEO-friendly metadata
- Industry-focused course catalog

## Tech Stack

- **React** 18.3.1 - JavaScript library for building user interfaces
- **Vite** 5.4.3 - Fast build tool and dev server
- **React Router** 6.26.1 - Client-side routing
- **Tailwind CSS** 4.0.0 - Utility-first CSS framework
- **shadcn/ui** - High-quality, accessible UI components
- **Lucide React** - Beautiful icon library

## Project Structure

```
jadv-professional-training/
├── public/
├── src/
│   ├── components/
│   │   ├── ui/
│   │   │   ├── Button.jsx
│   │   │   ├── Card.jsx
│   │   │   ├── Input.jsx
│   │   │   ├── Textarea.jsx
│   │   │   └── Label.jsx
│   │   ├── Navbar.jsx
│   │   ├── Footer.jsx
│   │   └── ThemeToggle.jsx
│   ├── context/
│   │   └── ThemeContext.jsx
│   ├── data/
│   │   └── courses.js
│   ├── lib/
│   │   └── utils.js
│   ├── pages/
│   │   ├── Home.jsx
│   │   ├── Courses.jsx
│   │   ├── CourseDetails.jsx
│   │   ├── About.jsx
│   │   └── Contact.jsx
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
├── index.html
├── package.json
├── vite.config.js
├── tailwind.config.js
└── README.md
```

## Installation & Setup

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn package manager

### Step 1: Install Dependencies

```bash
npm install
```

### Step 2: Configure Google Sheets Integration (Optional)

To enable form submissions to Google Sheets:

1. Follow the detailed setup guide in `GOOGLE_SHEETS_SETUP.md`
2. Update the Google Apps Script URL in `src/pages/Contact.jsx` (line 76)

If you skip this step, the form will still work but data won't be saved to Google Sheets.

### Step 3: Run Development Server

```bash
npm run dev
```

The application will start at `http://localhost:5173`

### Step 4: Build for Production

```bash
npm run build
```

The production-ready files will be generated in the `dist` folder.

### Step 5: Preview Production Build

```bash
npm run preview
```

## Available Scripts

- `npm run dev` - Start development server with hot reload
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally
- `npm run lint` - Run ESLint for code quality

## Pages Overview

### 1. Home Page (`/`)
- Hero section with call-to-action
- Popular courses preview
- Flexible training modes
- Why choose JADV section
- Student testimonials
- Final call-to-action

### 2. Courses Page (`/courses`)
- Complete course catalog
- Search functionality
- Course cards with key information
- Quick enroll buttons

### 3. Course Details Page (`/courses/:courseId`)
- Detailed course information
- Complete topic coverage list
- Training mode options
- Course features sidebar
- Enrollment call-to-action

### 4. About Us Page (`/about`)
- Institute statistics
- Mission and vision
- Company story
- Core values
- Why choose JADV

### 5. Contact/Enroll Page (`/contact`)
- Contact information
- Office hours
- Enrollment form with validation
- Success message on submission

## Customization

### Updating Course Data

Edit `src/data/courses.js` to:
- Add/remove courses
- Update course details
- Modify training modes
- Change testimonials

### Theme Customization

Edit `src/index.css` to customize:
- Color schemes (light and dark mode)
- Custom CSS variables
- Animation timings

### Component Styling

Components use Tailwind CSS classes and can be customized by:
- Modifying className props
- Updating the `cn()` utility function in `src/lib/utils.js`
- Editing Tailwind config in `tailwind.config.js`

## Deployment

### Deploy to Vercel

1. Install Vercel CLI:
```bash
npm install -g vercel
```

2. Deploy:
```bash
vercel
```

3. Follow the prompts to deploy your application.

### Deploy to Netlify

1. Build the project:
```bash
npm run build
```

2. Install Netlify CLI:
```bash
npm install -g netlify-cli
```

3. Deploy:
```bash
netlify deploy --prod --dir=dist
```

### Deploy to GitHub Pages

1. Install gh-pages:
```bash
npm install --save-dev gh-pages
```

2. Add to `package.json`:
```json
{
  "homepage": "https://yourusername.github.io/jadv-professional-training",
  "scripts": {
    "predeploy": "npm run build",
    "deploy": "gh-pages -d dist"
  }
}
```

3. Update `vite.config.js`:
```javascript
export default defineConfig({
  base: '/jadv-professional-training/',
  // ... rest of config
});
```

4. Deploy:
```bash
npm run deploy
```

### Deploy to Firebase Hosting

1. Install Firebase CLI:
```bash
npm install -g firebase-tools
```

2. Login and initialize:
```bash
firebase login
firebase init hosting
```

3. Configure `firebase.json`:
```json
{
  "hosting": {
    "public": "dist",
    "ignore": ["firebase.json", "**/.*", "**/node_modules/**"],
    "rewrites": [
      {
        "source": "**",
        "destination": "/index.html"
      }
    ]
  }
}
```

4. Build and deploy:
```bash
npm run build
firebase deploy
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Performance Optimizations

- Lazy loading for route components
- Optimized images and assets
- Minified CSS and JavaScript in production
- Tree-shaking with Vite

## Future Enhancements

- Add backend integration for form submissions
- Implement blog section
- Add student portal/dashboard
- Integrate payment gateway
- Add course reviews and ratings
- Implement live chat support

## License

This project is created for JADV Professional Training Institute. All rights reserved.

## Support

For questions or support, contact:
- Email: info@jadv.com
- Phone: +91 98765 43210

## Acknowledgments

- Built with [React](https://react.dev/)
- Styled with [Tailwind CSS](https://tailwindcss.com/)
- Icons from [Lucide](https://lucide.dev/)
- UI components inspired by [shadcn/ui](https://ui.shadcn.com/)
