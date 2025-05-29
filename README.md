# DeLightPlus UI

A collection of reusable React UI components by DeLightPlus.

## Installation

```bash
npm install delightplus-ui
# or
yarn add delightplus-ui
# or
pnpm add delightplus-ui
```

## Setup

### 1. Install Required Dependencies

Make sure you have the following peer dependencies installed in your project:

```bash
npm install react@^18.2.0 react-dom@^18.2.0
```

### 2. Configure Tailwind CSS

If you haven't already set up Tailwind CSS in your project, follow these steps:

1. Install Tailwind CSS and its dependencies:
```bash
npm install -D tailwindcss@^3.4.1 postcss@^8.4.35 autoprefixer@^10.4.17
```

2. Create a `tailwind.config.js` file in your project root:
```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    './src/**/*.{js,ts,jsx,tsx}',
    './node_modules/delightplus-ui/**/*.{js,ts,jsx,tsx}', // Add this line
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

3. Create a `postcss.config.js` file:
```js
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}
```

### 3. Import Styles

In your main application file (e.g., `src/app/layout.tsx` or `src/pages/_app.tsx`), import the DeLightPlus UI styles:

```tsx
// Import DeLightPlus UI styles
import 'delightplus-ui/dist/styles.css';
// Import your own Tailwind styles
import './globals.css';
```

## Usage

Import and use components in your React application:

```tsx
import { Button, Card, Container } from 'delightplus-ui';

function MyComponent() {
  return (
    <Container>
      <Card>
        <h2>Welcome to DeLightPlus UI</h2>
        <Button>Click me</Button>
      </Card>
    </Container>
  );
}
```

## Available Components

- `Button`: A customizable button component
- `Card`: A flexible card container
- `Container`: A responsive container component

## Development

To work on this package locally:

1. Clone the repository
2. Install dependencies:
```bash
npm install
```

3. Build the package:
```bash
npm run build
```

4. Link the package locally (in the package directory):
```bash
npm link
```

5. Link the package in your project:
```bash
npm link delightplus-ui
```

## Publishing

To publish a new version:

```bash
npm run release
```

This will:
1. Increment the patch version
2. Build the package
3. Publish to npm

## License

MIT © Kabelo Peter Matlakala

---
**Components**
- Button
- Modal (coming soon)
- Card (coming soon)

**Icons**
- HomeIcon
- SearchIcon

## Local Development
```bash
npm install
npm run build
```

License
MIT © DeLightPlus
---

![npm version](https://img.shields.io/npm/v/delightplus-ui)



<!--
---
🔹 To publish a new patch release:
```bash
npm run release
```
- Increments version from 0.1.2 → 0.1.3
- Builds the library
- Publishes it to NPM

🔹 To manually do a minor release:
```bash
npm run version:minor && npm run build && npm publish
```

---

When you release stable versions:
 ```bash
git tag v1.0.0
git push origin v1.0.0
``` -->
