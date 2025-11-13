# Prijava Repository - Copilot Instructions

## Repository Purpose
This repository manages claim data collection forms. Each claim is represented as a standalone HTML file containing form data, styling, and JavaScript for data collection and export functionality.

## File Structure
- Root directory contains claim HTML files named with pattern: `prijava_stete_*.html`
- `index.html` serves as the central hub listing all claim files with links
- `.github/` contains repository configuration and Copilot instructions

## Adding New Claim Files

When new claim HTML files are added to the repository:

1. **Detect new files**: Look for HTML files in the root directory matching the pattern `prijava_stete_*.html` or similar claim-related files
2. **Update index.html**: Automatically update the `index.html` file to include links to the new claim files
3. **Maintain alphabetical order**: Keep claim links sorted for easy navigation
4. **Extract metadata**: If possible, extract claim titles or identifiers from the HTML files to use as link text

## Index.html Maintenance

The `index.html` file should:
- Display a list of all claim files with clickable links
- Show a descriptive title for each claim (extracted from filename or file content)
- Be styled consistently with the claim forms
- Include a brief description of the repository purpose
- Be automatically updated when new files are added

## Code Style
- Use semantic HTML5 elements
- Keep JavaScript inline for simplicity (following existing file patterns)
- Use modern CSS with flexbox/grid for layouts
- Maintain responsive design for mobile devices
- Follow Serbian language conventions (lang="sr") as used in existing files

## Validation
- Ensure all HTML files are well-formed
- Verify all links in index.html point to existing files
- Check that new claim files follow the established structure

## Important Notes
- Each claim file is self-contained with its own styling and scripts
- Do not remove or modify existing claim files unless specifically requested
- Always maintain backward compatibility with existing claim links
