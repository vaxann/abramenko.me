# Ivan Abramenko - Personal Website

This repository contains a personal website for Ivan Abramenko built with Hugo, a static site generator. The site is multilingual (English and Russian) and uses the "hugo-coder" theme.

## Installation

### Prerequisites

To run this project locally, you'll need to have the following installed:

- [Hugo Extended](https://gohugo.io/installation/) (version 0.147.2 or newer)
- Git

### Setup Instructions

1. Clone the repository:

```bash
git clone https://github.com/vaxann/abramenko.me.git
cd abramenko.me
```

### Running Locally

To start a local development server with live-reload:

```bash
hugo server -D
```

This will make the site available at [http://localhost:1313](http://localhost:1313). The `-D` flag includes draft content.

### Building the Site

To build the static site for production:

```bash
hugo --minify
```

This will generate optimized files in the `public` directory.

## Multilingual Support

The site supports both English and Russian:

- English content is in the `content/` directory
- Russian content is in the `content/ru/` directory

## Adding Content

To add a new page:

```bash
# English version
hugo new content/pagename.md

# Russian version
hugo new content/ru/pagename.ru.md
```

## CSS Processing 

This project uses SCSS for styling. The repository contains pre-compiled CSS files in the `static/css-precompiled/` directory to support deployment on platforms that don't have Hugo Extended version available.

If you modify any SCSS files, you'll need to:

1. Rebuild locally with Hugo Extended
2. Copy the generated CSS files to the `static/css-precompiled/` directory
3. Commit these changes to the repository

## Deployment

### DigitalOcean App Platform

This project is configured to deploy automatically to DigitalOcean App Platform. The configuration is in the `.do/app.yaml` file.

When deploying to DigitalOcean, the application uses pre-compiled CSS files instead of requiring the Hugo Extended version.

## Project Structure

- `content/` - The main content files (English)
- `content/ru/` - Russian content files
- `static/` - Static files like images, CSS, etc.
- `layouts/` - Custom layout templates
- `themes/hugo-coder/` - The Hugo theme (included directly, not as a submodule)
- `config.toml` - Main site configuration
- `static/css-precompiled/` - Pre-compiled CSS files for deployment

## License

See the [LICENSE](LICENSE) file for details.