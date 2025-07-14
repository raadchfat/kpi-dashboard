# Service KPI Dashboard - GitHub Project Structure

## File Structure
```
service-kpi-dashboard/
├── public/
│   ├── index.html
│   ├── favicon.ico
│   └── manifest.json
├── src/
│   ├── components/
│   │   └── KPIDashboard.js
│   ├── App.js
│   ├── App.css
│   ├── index.js
│   └── index.css
├── package.json
├── package-lock.json
├── README.md
├── .gitignore
├── tailwind.config.js
└── postcss.config.js
```

## Installation & Setup

1. Clone the repository
2. Run `npm install` to install dependencies
3. Run `npm start` to start the development server
4. Open http://localhost:3000 in your browser

## Build for Production

Run `npm run build` to create an optimized production build.

---

## File Contents Below:

### package.json
```json
{
  "name": "service-kpi-dashboard",
  "version": "1.0.0",
  "description": "Business intelligence dashboard for service-based companies to analyze opportunity owner performance",
  "private": true,
  "dependencies": {
    "@testing-library/jest-dom": "^5.16.5",
    "@testing-library/react": "^13.4.0",
    "@testing-library/user-event": "^13.5.0",
    "lucide-react": "^0.263.1",
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-scripts": "5.0.1",
    "recharts": "^2.8.0",
    "xlsx": "^0.18.5",
    "web-vitals": "^2.1.4"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  },
  "eslintConfig": {
    "extends": [
      "react-app",
      "react-app/jest"
    ]
  },
  "browserslist": {
    "production": [
      ">0.2%",
      "not dead",
      "not op_mini all"
    ],
    "development": [
      "last 1 chrome version",
      "last 1 firefox version",
      "last 1 safari version"
    ]
  },
  "devDependencies": {
    "autoprefixer": "^10.4.14",
    "postcss": "^8.4.24",
    "tailwindcss": "^3.3.2"
  },
  "keywords": [
    "dashboard",
    "kpi",
    "business-intelligence",
    "service-business",
    "excel",
    "data-analysis",
    "react"
  ],
  "author": "Your Name",
  "license": "MIT",
  "homepage": "https://github.com/yourusername/service-kpi-dashboard"
}
```

### public/index.html
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <link rel="icon" href="%PUBLIC_URL%/favicon.ico" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <meta name="theme-color" content="#000000" />
    <meta
      name="description"
      content="Business intelligence dashboard for service-based companies to analyze opportunity owner performance"
    />
    <link rel="apple-touch-icon" href="%PUBLIC_URL%/logo192.png" />
    <link rel="manifest" href="%PUBLIC_URL%/manifest.json" />
    <title>Service KPI Dashboard</title>
  </head>
  <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
  </body>
</html>
```

### public/manifest.json
```json
{
  "short_name": "KPI Dashboard",
  "name": "Service KPI Dashboard",
  "icons": [
    {
      "src": "favicon.ico",
      "sizes": "64x64 32x32 24x24 16x16",
      "type": "image/x-icon"
    }
  ],
  "start_url": ".",
  "display": "standalone",
  "theme_color": "#000000",
  "background_color": "#ffffff"
}
```

### src/index.js
```javascript
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

### src/App.js
```javascript
import React from 'react';
import KPIDashboard from './components/KPIDashboard';
import './App.css';

function App() {
  return (
    <div className="App">
      <KPIDashboard />
    </div>
  );
}

export default App;
```

### src/App.css
```css
.App {
  text-align: center;
}

/* Additional custom styles can be added here */
```

### src/index.css
```css
@tailwind base;
@tailwind components;
@tailwind utilities;

body {
  margin: 0;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen',
    'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue',
    sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

code {
  font-family: source-code-pro, Menlo, Monaco, Consolas, 'Courier New',
    monospace;
}
```

### tailwind.config.js
```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./src/**/*.{js,jsx,ts,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
  safelist: [
    'border-blue-500',
    'border-green-500',
    'border-purple-500',
    'border-yellow-500',
    'border-red-500',
    'border-indigo-500',
    'bg-blue-100',
    'bg-green-100',
    'bg-purple-100',
    'bg-yellow-100',
    'bg-red-100',
    'bg-indigo-100',
    'text-blue-600',
    'text-green-600',
    'text-purple-600',
    'text-yellow-600',
    'text-red-600',
    'text-indigo-600',
  ]
}
```

### postcss.config.js
```javascript
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}
```

### .gitignore
```
# Dependencies
/node_modules
/.pnp
.pnp.js

# Testing
/coverage

# Production
/build

# Misc
.DS_Store
.env.local
.env.development.local
.env.test.local
.env.production.local

# Logs
npm-debug.log*
yarn-debug.log*
yarn-error.log*

# IDE
.vscode/
.idea/
*.swp
*.swo

# OS
Thumbs.db
```

### README.md
```markdown
# Service KPI Dashboard

A comprehensive business intelligence dashboard for service-based companies to analyze opportunity owner performance across key metrics.

## Features

- **Multi-file Excel/CSV Support**: Upload and process Jobs, Appointments, and Invoices data
- **Smart Data Integration**: Automatically matches data across files using common identifiers
- **Six Key KPIs**: Hydro Jetting Sold, Descaling Sold, On-Time Arrival Rate, 5★ Reviews, Warranty Call Rate, Upsell Conversion Rate
- **Interactive Visualizations**: Bar charts, service breakdowns, and detailed tables
- **Data Quality Reporting**: Comprehensive validation and quality indicators
- **Responsive Design**: Works on desktop and mobile devices

## Supported File Formats

- Excel (.xlsx, .xls)
- CSV (.csv)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/service-kpi-dashboard.git
   cd service-kpi-dashboard
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser

## Usage

1. **Upload Files**: Add your three data files (Jobs, Appointments, Invoices)
2. **Process Data**: Click "Process Data & Generate KPIs" to analyze
3. **View Results**: Explore KPI cards, charts, and detailed tables
4. **Filter Results**: Use the dropdown to focus on specific opportunity owners

## Data Structure

The dashboard intelligently maps common column variations:

- **IDs**: job_id, appointment_id, technician_id, invoice_id
- **Owner**: opportunity_owner, technician, tech_name, employee_name
- **Services**: service_type, description, services
- **Timing**: scheduled_time, arrival_time
- **Reviews**: review_rating, rating
- **Warranty**: warranty_eligible, warranty_call
- **Upsells**: upsell_opportunity, upsell_converted

## Build for Production

```bash
npm run build
```

This creates a `build` folder with optimized production files.

## Technologies Used

- React 18
- Tailwind CSS
- Recharts (for visualizations)
- SheetJS (for Excel parsing)
- Lucide React (for icons)

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, please open an issue in the GitHub repository.
```

## Next Steps

1. Create a new GitHub repository
2. Copy each file to its respective location
3. Run `npm install` to install dependencies
4. Start development with `npm start`
5. Deploy to services like Netlify, Vercel, or GitHub Pages

This project structure provides a complete, production-ready React application with all the necessary configuration files for modern development workflows.
