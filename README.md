# UIVault

A production-ready React component library with TypeScript and Tailwind CSS. Build beautiful, accessible interfaces with reusable components.

## 📦 Components

### Button

Customizable button component with multiple variants and sizes.

```tsx
import { Button } from '@uivault/components';

<Button variant="primary" size="lg">
  Click me
</Button>

<Button variant="danger" disabled>
  Disabled
</Button>

<Button variant="ghost" loading>
  Loading
</Button>
```

**Props:**
- `variant`: 'primary' | 'secondary' | 'danger' | 'ghost'
- `size`: 'sm' | 'md' | 'lg'
- `loading`: boolean
- `disabled`: boolean

### Card

Container component with optional header, body, and footer sections.

```tsx
import { Card, CardHeader, CardBody, CardFooter } from '@uivault/components';

<Card>
  <CardHeader>
    <h2>Card Title</h2>
  </CardHeader>
  <CardBody>
    Card content goes here
  </CardBody>
  <CardFooter>
    <Button>Action</Button>
  </CardFooter>
</Card>
```

**Variants:**
- `default`: Basic shadow
- `elevated`: Enhanced shadow
- `outlined`: Border-based

### Badge

Small component for labels and tags.

```tsx
import { Badge } from '@uivault/components';

<Badge variant="primary">New</Badge>
<Badge variant="success" size="lg">Active</Badge>
<Badge variant="danger">Critical</Badge>
```

**Props:**
- `variant`: 'default' | 'primary' | 'success' | 'warning' | 'danger'
- `size`: 'sm' | 'md' | 'lg'

## 🚀 Installation

```bash
npm install @uivault/components
```

## 🎨 Features

- ✅ **TypeScript**: Full type safety and autocomplete
- ✅ **Tailwind CSS**: Easy to customize and extend
- ✅ **Accessible**: WCAG 2.1 compliant components
- ✅ **Dark Mode Ready**: Works with Tailwind dark mode
- ✅ **Zero Runtime**: Ships as React components
- ✅ **Tree-Shakeable**: Only import what you use

## 📁 Project Structure

```
uivault/
├── src/
│   ├── components/
│   │   ├── Button.tsx
│   │   ├── Card.tsx
│   │   ├── Badge.tsx
│   │   └── ...
│   └── index.ts
├── dist/               # Built files
├── vite.config.ts      # Build configuration
├── tsconfig.json       # TypeScript config
└── package.json
```

## 🏗️ Build & Publish

```bash
# Install dependencies
npm install

# Build the library
npm run build

# Output: dist/
# - dist/index.mjs (ES modules)
# - dist/index.js (CommonJS)
# - dist/index.d.ts (TypeScript declarations)
```

### Publish to NPM

```bash
# Login to npm
npm login

# Publish
npm publish
```

## 🎯 Component Development

### Creating a New Component

1. Create component file: `src/components/MyComponent.tsx`
2. Export from `src/index.ts`
3. Add TypeScript types
4. Test with sample props
5. Update README with usage

### Example

```tsx
import React from 'react';

interface MyComponentProps {
  label: string;
  variant?: 'primary' | 'secondary';
}

export const MyComponent: React.FC<MyComponentProps> = ({
  label,
  variant = 'primary',
}) => {
  return <div className={`component-${variant}`}>{label}</div>;
};
```

## 🧪 Testing

```bash
# Type check
npm run type-check
```

## 📚 Customization

### Override Tailwind Colors

In your project's `tailwind.config.js`:

```js
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: '#007bff',
      },
    },
  },
};
```

### Dark Mode

Components support Tailwind's dark mode out of the box:

```tsx
<div className="dark">
  <Button>Works in dark mode</Button>
</div>
```

## 🚀 Future Components

- [ ] Input field with validation
- [ ] Dropdown/Select
- [ ] Modal/Dialog
- [ ] Toast notifications
- [ ] Tabs
- [ ] Accordion
- [ ] Breadcrumbs
- [ ] Pagination
- [ ] Form components
- [ ] Data table
- [ ] Calendar picker
- [ ] Tooltip

## 📦 Distribution

This library is distributed in multiple formats:

- **ES Modules**: `dist/index.mjs` (modern browsers)
- **CommonJS**: `dist/index.js` (Node.js)
- **TypeScript**: `dist/index.d.ts` (type definitions)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

MIT License - feel free to use in your projects.

## 📞 Support

For issues, feature requests, or questions, please open an issue on GitHub.

---

**Status**: ✅ Production Ready  
**Version**: 1.0.0  
**Last Updated**: February 2026
