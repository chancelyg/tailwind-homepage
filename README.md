# Personal Navigation Homepage

A simple and elegant personal navigation page built with HTML, TailwindCSS, and YAML configuration.

## Project Structure

```
.
├── config.yaml        # Site configuration file (categories and links)
├── index.html        # Main application page
├── .vscode/         # VS Code configuration
└── README.md        # Project documentation
```

## Features

- Clean and responsive design using TailwindCSS
- Configurable categories and links via YAML
- Real-time search functionality
- Hover effects and modern UI

## Setup and Running

1. Clone this repository
2. Make sure you have Python installed (Python 3.x recommended)
3. Run the development server:
   ```bash
   python -m http.server
   ```
4. Open your browser and visit `http://localhost:8000`

## Configuration

Edit `config.yaml` to customize your navigation links:

```yaml
categories:
  - name: Category Name
    color: indigo-600
    sites:
      - name: Site Name
        url: https://example.com
        icon: EX
        iconBg: bg-blue-500
        iconColor: text-white
```

## Development

This project uses:
- TailwindCSS (via CDN)
- js-yaml for YAML parsing
- Python's built-in HTTP server for development

VS Code launch configuration is included for easy debugging.