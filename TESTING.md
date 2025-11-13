# How to Test the Copilot Instructions Setup

This document explains how to verify that the Copilot instructions are working correctly.

## What Was Set Up

1. **`.github/copilot-instructions.md`** - Instructions that tell GitHub Copilot how to handle new claim files
2. **`index.html`** - A central hub that lists all claim files

## How to Test

### Method 1: Add a New Claim File via GitHub Web Interface

1. **Upload a new HTML file** to the repository root with a name matching the pattern `prijava_stete_*.html`
   - Example: `prijava_stete_auto_123456.html` or `prijava_stete_kuca_654321.html`

2. **Create an issue or mention @copilot** in a comment asking to update the index:
   ```
   @copilot Please update index.html to include the new file I just added
   ```

3. **Check the PR** that Copilot creates - it should:
   - Add a new `<li>` entry in `index.html`
   - Extract the title from your new file
   - Keep the list in alphabetical order

### Method 2: Test with GitHub Copilot Agent

1. **Create an issue** with:
   ```
   @copilot I added a new file prijava_stete_test_999999.html. 
   Please update index.html to include it.
   ```

2. **Copilot should automatically**:
   - Detect the new file
   - Read its title (from `<title>` tag or filename)
   - Update `index.html` with a properly formatted link
   - Create a PR with the changes

### Method 3: Manual Verification

1. **Add any HTML file** matching `prijava_stete_*.html` to the repository

2. **Open an issue** asking Copilot to update the index

3. **Verify the result**:
   - Check that `index.html` now includes your file
   - Verify the link works and points to the correct file
   - Confirm the styling matches existing entries

## Expected Result

When Copilot updates `index.html`, you should see a new entry like:

```html
<li class="claim-item">
    <a href="prijava_stete_NEW_FILE.html" class="claim-link">
        <span>Title Extracted from File</span>
    </a>
</li>
```

## Current State

- **Files in repository**: 3 claim files (`prijava_stete_zivina_806411.html`, `prijava_stete_zivina_806435.html`, `prijava_stete_zivina_807443.html`)
- **Listed in index.html**: ✅ Yes (all 3 files)
- **Copilot instructions**: ✅ Active in `.github/copilot-instructions.md`

## Next Steps

Simply add your next claim file and mention @copilot to test the automatic update functionality!
