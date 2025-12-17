# Sidebar-1

A modern, responsive two-level sidebar component built with React, TypeScript, and Tailwind CSS. Features collapsible navigation, dynamic content sections, and smooth spring animations.

## Features

- **Two-Level Navigation**: Icon-based primary navigation with expandable detailed secondary navigation
- **Collapsible Design**: Sidebar can collapse to show only icons for space efficiency
- **Dynamic Content**: Each navigation section displays unique content and sub-items
- **Smooth Animations**: Soft spring easing for all transitions
- **Fully Responsive**: Adapts to different screen sizes
- **Dark Theme**: Modern dark UI with neutral color palette
- **Search Functionality**: Built-in search bar that adapts to collapsed state
- **Expandable Menu Items**: Support for nested menu items with dropdown functionality

## Technology Stack

- React 18
- TypeScript
- Tailwind CSS v4.0
- Carbon Icons React
- Vite (development)

## Project Structure

```
├── App.tsx                          # Main application entry
├── components/
│   ├── SidebarDemo.tsx             # Main sidebar implementation
│   ├── figma/
│   │   └── ImageWithFallback.tsx   # Image fallback component
│   └── ui/                         # UI component library
├── imports/
│   ├── Frame760.tsx                # Exported frame component
│   └── svg-svkvdgwod6.ts          # SVG path definitions
├── styles/
│   └── globals.css                 # Global styles and Tailwind config
└── Attributions.md                 # Third-party attributions
```

## Components Overview

### TwoLevelSidebar
The main sidebar component that combines icon navigation and detail panels.

### IconNavigation
Left sidebar with icon-based navigation items for main sections:
- Dashboard
- Tasks
- Projects
- Calendar
- Teams
- Analytics
- Files
- Settings

### DetailSidebar
Right sidebar that displays detailed content based on selected section:
- Collapsible title header
- Search container
- Multiple menu sections with expandable items
- Smooth state transitions

### Key Features

**Search Container**
- Integrated search input
- Adapts to collapsed state
- Smooth opacity transitions

**Menu Items**
- Icon-based navigation
- Support for dropdown/expandable items
- Active state highlighting
- Tooltip support when collapsed

**Animations**
- Custom spring easing: `cubic-bezier(0.25, 1.1, 0.4, 1)`
- 500ms transition duration
- Synchronized width, opacity, and transform animations

## Getting Started

### Installation

```bash
npm install
```

### Development

```bash
npm run dev
```

### Build

```bash
npm run build
```

## Usage Example

```tsx
import { Frame760 } from "./components/SidebarDemo";

export default function App() {
  return <Frame760 />;
}
```

## Customization

### Adding New Sections

Edit the `getSidebarContent` function in `SidebarDemo.tsx` to add new navigation sections:

```tsx
const contentMap: Record<string, SidebarContent> = {
  yourSection: {
    title: "Your Section",
    sections: [
      {
        title: "Section Title",
        items: [
          {
            icon: <YourIcon size={16} className="text-neutral-50" />,
            label: "Item Label",
            hasDropdown: true,
            children: [
              { label: "Sub Item 1" },
              { label: "Sub Item 2" },
            ],
          },
        ],
      },
    ],
  },
};
```

### Styling

The component uses Tailwind CSS v4.0 with custom CSS variables defined in `styles/globals.css`. Key color variables:

- `--background`: Main background color
- `--foreground`: Main text color
- `--neutral-*`: Grayscale palette for UI elements
- `--sidebar-*`: Sidebar-specific color tokens

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

MIT

## Attributions

This project includes:
- Components from [shadcn/ui](https://ui.shadcn.com/) under [MIT license](https://github.com/shadcn-ui/ui/blob/main/LICENSE.md)
- Photos from [Unsplash](https://unsplash.com) under [Unsplash license](https://unsplash.com/license)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
