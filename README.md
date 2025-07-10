# Kinsta MU Plugins

This repository contains the Kinsta Must-Use Plugins, automatically synced from the official Kinsta distribution.

## About

This is a mirror repository that automatically downloads and tracks updates from the official Kinsta MU Plugin package available at: https://kinsta.com/kinsta-tools/kinsta-mu-plugins.zip

The repository is automatically updated weekly via GitHub Actions when a new version is detected.

## Usage with Composer

You can use this repository as a VCS package in your Composer-based WordPress project instead of manually downloading the zip file.

### Add to composer.json

Add this repository to your `composer.json`:

```json
{
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/yourdigitaltoolbox/kinsta-mu-plugin"
        }
    ],
    "require": {
        "kinsta/kinsta-mu-plugins": "^3.2"
    },
}
```

### Install

```bash
composer install
```

This will automatically install the latest version of the Kinsta MU Plugin into your mu-plugins directory.

## Automatic Updates

The repository uses GitHub Actions to automatically:

1. Check for updates weekly (every Monday at 9:00 AM UTC)
2. Download the latest version from Kinsta
3. Compare versions and update if necessary
4. Commit changes and create version tags
5. Preserve repository-specific files (`.git`, `.github`, `README.md`, `composer.json`, `.gitignore`, `.gitattributes`)

The `.gitattributes` file ensures that when installed via Composer, only the essential plugin files are included, excluding development files like `.github/` workflows.

You can also manually trigger the update workflow from the GitHub Actions tab.

## Version History

Version tags are automatically created for each update, allowing you to pin to specific versions or use version constraints in Composer.

## License

This plugin is provided by Kinsta. Please refer to Kinsta's terms of service for licensing information.

## Support

For support with the Kinsta MU Plugin itself, please contact [Kinsta Support](https://kinsta.com/help/).

For issues with this repository or the automated updates, please open an issue on GitHub.
