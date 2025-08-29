# Deno Wallabag Server

This is a [Wallabag](https://github.com/wallabag/wallabag) server implementation using Deno, TypeScript, and Fresh framework. It improves web capture using Playwright and AI technologies.

Wallabag is a self-hostable application for saving web pages for later reading. This implementation provides the same core functionality with modern web technologies and enhanced features.

![Wallabag Interface](https://raw.githubusercontent.com/wallabag/wallabag/master/.github/images/screenshot.png)

## Features

- **Web Page Saving**: Save articles and web pages for offline reading
- **Content Extraction**: Extract clean content without distractions like ads and pop-ups
- **Self-Hosted**: Run on your own server for complete privacy
- **API Compatibility**: Compatible with Wallabag API for existing clients
- **Data Import**: Import data from existing Wallabag instances
- **Enhanced Web Capture**: Improved capture using Playwright and AI
- **Responsive Design**: Works on desktop and mobile devices
- **Tagging System**: Organize your saved articles with tags
- **Search Functionality**: Find your saved articles quickly
- **Reading Time Estimation**: See how long articles will take to read

## Technology Stack

- **Deno**: Modern runtime for JavaScript and TypeScript
- **Fresh**: Next generation web framework for Deno
- **TypeScript**: Strongly typed programming language that builds on JavaScript
- **Tailwind CSS**: Utility-first CSS framework
- **Playwright**: Browser automation library for enhanced web capture
- **AI Integration**: Machine learning for improved content processing

## Prerequisites

- [Deno](https://deno.land/manual/getting_started/installation) installed on your system

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/deno-wallabag-server.git
   cd deno-wallabag-server
   ```

2. Install dependencies (Deno will automatically handle this):
   ```bash
   deno task start
   ```

## Usage

### Starting the Server

Make sure to install Deno: https://deno.land/manual/getting_started/installation

Then start the project:

```bash
deno task start
```

This will watch the project directory and restart as necessary.

### Importing Data from Another Wallabag Instance

To import data from another Wallabag instance:

1. Obtain your API credentials from the source Wallabag instance
2. Configure the connection settings in your environment variables:
   ```bash
   export WALLABAG_CLIENT_ID=your_client_id
   export WALLABAG_CLIENT_SECRET=your_client_secret
   export WALLABAG_USERNAME=your_username
   export WALLABAG_PASSWORD=your_password
   export WALLABAG_BASE_URL=https://your-wallabag-instance.com
   ```
3. Run the import script:
   ```bash
   deno task import-data
   ```

### API Endpoints

This implementation provides API compatibility with the original Wallabag project:

- `GET /api/entries` - Retrieve saved entries
- `POST /api/entries` - Save a new entry
- `GET /api/entries/{id}` - Retrieve a specific entry
- `PUT /api/entries/{id}` - Update an entry
- `DELETE /api/entries/{id}` - Delete an entry
- `GET /api/tags` - Retrieve tags
- `POST /api/tags` - Create a new tag

For detailed API documentation, please refer to the [Wallabag API documentation](https://doc.wallabag.org/en/developer/api/).

## Development

### Project Structure

```
.
├── components/         # Shared UI components
├── islands/            # Interactive client-side components
├── routes/             # Page routes and API endpoints
├── static/             # Static assets
├── deno.json           # Deno configuration
├── fresh.config.ts     # Fresh framework configuration
├── main.ts             # Application entry point
└── dev.ts              # Development server configuration
```

### Available Scripts

- `deno task start` - Start the development server
- `deno task build` - Build the application for production
- `deno task preview` - Preview the built application
- `deno task check` - Run formatting, linting, and type checking

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Related Projects

- [Wallabag](https://github.com/wallabag/wallabag) - Original PHP implementation
- [Wallabag Android App](https://github.com/wallabag/android-app)
- [Wallabag iOS App](https://github.com/wallabag/ios-app)
- [Wallabagger Browser Extension](https://github.com/wallabag/wallabagger)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the Wallabag team for creating such a useful application
- Content extraction relies on Playwright and AI technologies
- Inspired by the original Wallabag project and its community