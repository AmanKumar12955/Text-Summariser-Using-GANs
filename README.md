# Advanced Text Summarization Using Generative Adversarial Networks

## Project Overview
This project demonstrates an advanced text summarization technique using Generative Adversarial Networks (GANs).

## Prerequisites
- Visual Studio Code (VS Code)
- Node.js (v18 or later recommended)
- npm (Node Package Manager)

## Setting Up the Project in VS Code

### 1. Clone the Repository
Open Terminal in VS Code and run:
```bash
git clone <YOUR_REPOSITORY_URL>
cd gan-text-summarizer
```

### 2. Install Extensions
Recommended VS Code extensions:
- ESLint
- Prettier - Code formatter
- Tailwind CSS IntelliSense
- TypeScript Vue Plugin (Volar)

### 3. Install Dependencies
```bash
npm install
```

### 4. Configure Environment (if needed)
- Create a `.env` file in the project root
- Add any required environment variables

### 5. Run the Development Server
```bash
npm run dev
```
- The application will be available at `http://localhost:8080`

### 6. Build for Production
```bash
npm run build
```

### 7. Recommended Workspace Settings
Create or update `.vscode/settings.json`:
```json
{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "typescript.tsdk": "node_modules/typescript/lib"
}
```

## Changing Browser URL and Routing

### Modifying Routes
To change the browser URL and add new routes to the application:

1. Open `src/App.tsx`
2. Locate the `<Routes>` component
3. Add new `<Route>` components with desired paths

Example of adding a new route:
```tsx
<Routes>
  <Route path="/" element={<Index />} />
  <Route path="/summary" element={<SummaryPage />} />
  <Route path="/methodology" element={<MethodologyPage />} />
  {/* ADD ALL CUSTOM ROUTES ABOVE THE CATCH-ALL "*" ROUTE */}
  <Route path="*" element={<NotFound />} />
</Routes>
```

### Navigation Methods
Use these methods to change URLs:

1. **React Router's `Link` Component**:
```tsx
import { Link } from 'react-router-dom';

// In your component
<Link to="/summary">View Summary</Link>
```

2. **Programmatic Navigation**:
```tsx
import { useNavigate } from 'react-router-dom';

const MyComponent = () => {
  const navigate = useNavigate();
  
  const handleNavigation = () => {
    navigate('/methodology');
  };
};
```

### URL Parameters
To create dynamic routes with parameters:
```tsx
<Route path="/summary/:id" element={<SummaryDetail />} />
```

### Accessing URL Parameters
```tsx
import { useParams } from 'react-router-dom';

const SummaryDetail = () => {
  const { id } = useParams();
  // Use the id parameter
};
```

## Troubleshooting
- Ensure Node.js and npm are correctly installed
- Check console for any dependency or build errors
- Verify all npm scripts in `package.json`

## Learn More
- [Project Documentation](https://docs.lovable.dev)
- [GAN Research Paper](# Add your research paper link)

## Contributing
Please read our contribution guidelines before submitting pull requests.

## License
[Add your license information]
