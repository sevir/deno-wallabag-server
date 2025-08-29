# Copilot Instructions for Deno Wallabag Server

This document provides instructions for GitHub Copilot to better understand and assist with the development of the Deno Wallabag Server project.

## Project Overview

This is a Wallabag server implementation using Deno, TypeScript, and the Fresh framework. It aims to provide the same functionality as the original PHP-based Wallabag but with modern web technologies and enhanced features like improved web capture using Playwright and AI.

## Technology Stack

- **Deno**: Runtime for JavaScript and TypeScript
- **Fresh**: Web framework for Deno
- **TypeScript**: Primary programming language
- **Tailwind CSS**: Styling framework
- **Playwright**: For enhanced web page capture

## Project Structure

```
.
├── components/         # Shared UI components
├── islands/            # Interactive client-side components
├── routes/             # Page routes and API endpoints
│   ├── api/            # API endpoints
│   └── greet/          # Example routes
├── static/             # Static assets (images, stylesheets)
├── deno.json           # Deno configuration
├── fresh.config.ts     # Fresh framework configuration
├── main.ts             # Application entry point
└── dev.ts              # Development server configuration
```

## Development Guidelines

### Code Style

- Use TypeScript for all server-side code
- Follow functional programming patterns where possible
- Use Preact signals for state management in islands
- Use Tailwind CSS for styling

### API Development

When adding new API endpoints:

1. Place them in the `routes/api/` directory
2. Follow RESTful conventions
3. Use proper HTTP status codes
4. Return JSON responses
5. Implement proper error handling

Example API endpoint structure:
```typescript
import { FreshContext } from "$fresh/server.ts";

export const handler = async (req: Request, ctx: FreshContext): Response => {
  // API logic here
  return new Response(JSON.stringify({ message: "Success" }), {
    headers: { "Content-Type": "application/json" },
  });
};
```

### UI Components

When creating new UI components:

1. Place them in the `components/` directory
2. Use TypeScript with proper type annotations
3. Use Tailwind CSS for styling
4. Make components reusable and configurable via props

### Islands

When creating interactive client-side components:

1. Place them in the `islands/` directory
2. Use Preact signals for state management
3. Keep islands focused on specific interactive functionality

## Common Tasks

### Adding a New API Endpoint

1. Create a new file in `routes/api/` directory
2. Export a `handler` function that handles the request
3. Implement proper error handling and validation
4. Return appropriate HTTP status codes

### Adding a New UI Component

1. Create a new file in `components/` directory
2. Export a function component with proper TypeScript types
3. Use Tailwind CSS classes for styling
4. Make the component reusable with props

### Adding a New Island

1. Create a new file in `islands/` directory
2. Export a default function component
3. Use Preact signals for state management
4. Focus on specific interactive functionality

## Environment Variables

The application may use the following environment variables:

- `WALLABAG_CLIENT_ID` - Client ID for Wallabag API
- `WALLABAG_CLIENT_SECRET` - Client secret for Wallabag API
- `WALLABAG_USERNAME` - Username for Wallabag API
- `WALLABAG_PASSWORD` - Password for Wallabag API
- `WALLABAG_BASE_URL` - Base URL for Wallabag instance

## Data Import Feature

The application includes a feature to import data from another Wallabag instance. This feature:

1. Uses OAuth2 for authentication with the source instance
2. Fetches entries using the Wallabag API
3. Maps the data to the local data structure
4. Stores the imported data in the local database

When working on this feature, ensure compatibility with the Wallabag API specification.

## Testing

When adding new features or fixing bugs:

1. Consider adding tests for API endpoints
2. Test UI components in isolation
3. Verify cross-browser compatibility
4. Test responsive design on different screen sizes

## Deployment

The application can be deployed using Deno Deploy or other Deno-compatible hosting services. Ensure all environment variables are properly configured in the deployment environment.

## References

- [Wallabag Documentation](https://doc.wallabag.org/)
- [Deno Documentation](https://deno.land/manual)
- [Fresh Framework Documentation](https://fresh.deno.dev/docs)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)