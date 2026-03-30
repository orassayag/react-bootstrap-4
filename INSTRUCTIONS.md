# Instructions

## Setup Instructions

1. Open the project in your IDE (VSCode recommended)
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm start
   ```

## Project Configuration

This project is built with Create React App and includes custom webpack configuration. Key configuration files:
- `package.json` - Dependencies and scripts
- `config/` - Webpack and build configurations
- `scripts/` - Build and development scripts

## Available Scripts

### Start Development Server
Runs the app in development mode with hot reloading:
```bash
npm start
```
Opens [http://localhost:3000](http://localhost:3000) in your browser.

### Build for Production
Creates an optimized production build:
```bash
npm run build
```
Output will be in the `build/` directory.

### Run Tests
Launches the test runner in interactive watch mode:
```bash
npm test
```

## Project Structure

### Source Files (`src/`)
- `containers/` - Page-level React components
  - `App/` - Main application container with routing
  - `Home/` - Home page with album example
- `hoc/` - Higher-order components
  - `Layout/` - Layout wrapper component
  - `Auxiliary/` - Auxiliary wrapper component
- `index.js` - Application entry point
- `serviceWorker.js` - PWA service worker

### Style Files
- `*.scss` - Component-specific styles using SCSS
- Bootstrap 4 is imported globally in `index.js`

### Public Files (`public/`)
- `index.html` - HTML template
- `manifest.json` - PWA manifest
- `favicon.ico` - Application icon

## Creating New Components

### Container Component
1. Create a new folder in `src/containers/`
2. Create component file: `ComponentName.jsx`
3. Create style file: `ComponentName.scss`
4. Export from `src/containers/index.js`

Example:
```jsx
import React, { Component } from 'react';
import PropTypes from 'prop-types';
import { Auxiliary } from '../../hoc';
import './ComponentName.scss';

const propTypes = {
    // Define your prop types
};

class ComponentName extends Component {
    state = {
        // Define your state
    };

    render() {
        return (
            <Auxiliary>
                {/* Your component JSX */}
            </Auxiliary>
        );
    }
}

ComponentName.propTypes = propTypes;

export default ComponentName;
```

### Adding Routes
Update `src/containers/App/App.jsx`:
```jsx
<Route path="/your-path" exact component={containers.YourComponent} />
```

## Using Bootstrap Components

This project includes Bootstrap 4. Use Bootstrap classes directly in your JSX:
```jsx
<div className="container">
    <div className="row">
        <div className="col-md-6">
            <button className="btn btn-primary">Click Me</button>
        </div>
    </div>
</div>
```

## Custom Styling with SCSS

Create component-specific SCSS files:
```scss
.component-name {
    // Your styles
    &__element {
        // Element styles
    }
    
    &--modifier {
        // Modifier styles
    }
}
```

## Environment Variables

Create a `.env` file in the root directory:
```
REACT_APP_API_URL=your_api_url_here
```

Access in your code:
```javascript
const apiUrl = process.env.REACT_APP_API_URL;
```

## Building for Production

1. Run the build command:
   ```bash
   npm run build
   ```
2. The optimized build will be in the `build/` folder
3. Deploy the contents of the `build/` folder to your hosting service

## Browser Compatibility

The app is configured to support:
- Modern browsers (>0.2% market share)
- Excludes IE 11 and below
- Excludes Opera Mini

## Development Tips

1. **Hot Reloading**: Changes to source files will automatically reload the browser
2. **CSS Modules**: SCSS files are locally scoped to components
3. **PropTypes**: Always validate component props
4. **State Management**: Use component state or add Redux if needed
5. **React Router**: Add new routes in `App.jsx`

## Notes

- The project uses Create React App configuration
- Webpack is pre-configured with optimizations
- Service worker is disabled by default (can be enabled in `index.js`)
- Bootstrap 4 is included as a dependency
- Node-sass is used for SCSS compilation

## Author

* **Or Assayag** - *Initial work* - [orassayag](https://github.com/orassayag)
* Or Assayag <orassayag@gmail.com>
* GitHub: https://github.com/orassayag
* StackOverflow: https://stackoverflow.com/users/4442606/or-assayag?tab=profile
* LinkedIn: https://linkedin.com/in/orassayag
