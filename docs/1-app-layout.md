# AppLayout

1. According screensot , to build App layout

The App Layout component provides a flexible layout structure with a collapsible sidebar and main content area, similar to the GitHub Trending interface shown in the screenshot. It's designed to create a consistent layout across your application.

## Features

- Collapsible sidebar with smooth transitions
- Responsive design
- Customizable sidebar content
- Clean, modern UI matching GitHub's aesthetic

## Usage

```tsx
import { AppLayout } from "@/components/app-layout"

export default function RootLayout({
  children,
}: {
  children: React.ReactNode
}) {
  return (
    <AppLayout
      sidebar={
        <nav className="p-4">
          <div className="mb-8">
            {/* Logo or branding */}
          </div>
          <div className="space-y-4">
            {/* Navigation sections */}
            <div>
              <h2 className="mb-2 text-lg font-semibold">Navigation</h2>
              <ul className="space-y-2">
                <li>Trending</li>
                <li>Languages</li>
                <li>Topics</li>
              </ul>
            </div>
          </div>
        </nav>
      }
    >
      {children}
    </AppLayout>
  )
}
```

## Props

- `children`: The main content to be rendered in the layout
- `sidebar`: Optional sidebar content
- `className`: Optional additional CSS classes for the sidebar
- Additional HTML div props are passed to the sidebar container

## Customization

The layout uses Tailwind CSS classes and can be customized by modifying the className props or extending the component.

### Default Measurements

- Expanded sidebar width: 16rem (w-64)
- Collapsed sidebar width: 4rem (w-16)
- Sidebar transition: All properties animate smoothly

### Styling

The layout uses your application's color scheme through CSS variables:

- Background: bg-background
- Border: border-r
- Text: Inherits from parent