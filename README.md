# FabFilter - uBlock Origin Filter for fab.com

A simple uBlock Origin filter to block specific creators and assets on fab.com (Epic Games' digital content marketplace).

## What This Filter Does

This filter provides a simple way to:
1. **Block specific creators by name** - Hide all assets from creators you want to avoid
2. **Block specific assets by listing ID** - Hide individual problematic assets

## Installation

### Method 1: Direct Filter Import
1. Install uBlock Origin browser extension
2. Open uBlock Origin dashboard
3. Go to "Filter lists" tab
4. Click "Import" and add the filter URL or paste the filter content
5. Apply changes

### Method 2: Manual Installation
1. Copy the contents of `fab-filter.txt`
2. Open uBlock Origin dashboard
3. Go to "My filters" tab
4. Paste the filter rules
5. Apply changes

## How to Use

### Block a Creator
1. Find the creator's name on fab.com (shown under asset titles)
2. Add this rule to uBlock Origin's "My filters":
```
fab.com##.fabkit-Stack-root.nTa5u2sc:has(.qiXoiquf .fabkit-Typography-ellipsisWrapper:has-text("CreatorName"))
```
3. Replace "CreatorName" with the exact name as shown on the site

### Block a Specific Asset
1. Go to the asset page on fab.com
2. Copy the listing ID from the URL (the UUID after `/listings/`)
3. Add this rule to uBlock Origin's "My filters":
```
fab.com##a.bc6TaIqU[href*="/listings/YOUR-LISTING-ID"]:upward(.fabkit-Stack-root.nTa5u2sc)
```
4. Replace "YOUR-LISTING-ID" with the actual ID

### Example Rules
```
! Block a creator named "BadActor"
fab.com##.fabkit-Stack-root.nTa5u2sc:has(.qiXoiquf .fabkit-Typography-ellipsisWrapper:has-text("BadActor"))

! Block a specific asset
fab.com##a.bc6TaIqU[href*="/listings/61709449-01ea-4d55-9051-7f8f68dd1f1d"]:upward(.fabkit-Stack-root.nTa5u2sc)
```

## Usage

### Identifying Problematic Sellers
1. Browse fab.com normally
2. When you encounter suspicious content, note the seller information
3. Create a new issue or pull request in this repository.
4. Report the seller to Epic Games / Fab if you find them violating platform rules.

### Updating Filters
1. Regularly update the filter list to catch new problematic sellers
2. Community contributions are welcome via pull requests

### Reporting False Positives
If legitimate content is being blocked:
1. Check the seller against the list
2. Review the keyword filters for overly broad terms
3. Submit an issue with details about the false positive

## Contributing

### Adding New Filters
1. Fork the repository
2. Test your filters on fab.com
3. Add appropriate documentation
4. Submit a pull request

### Reporting Issues
1. Provide the specific URL where the issue occurs
2. Include screenshots if possible
3. Describe the expected vs actual behavior
4. Include your browser and uBlock Origin version

**Note**: This tool is for personal use only. Always verify content legitimacy through official channels before making purchases.

## Disclaimer

- This filter is not affiliated with Epic Games or fab.com
- Blocking decisions are based on heuristics and may have false positives
- Users should still exercise due diligence when purchasing assets
- The filter does not guarantee complete protection against all problematic content

## Support

For support and updates:
- Check the GitHub issues page
- Join the community discussions
- Follow the project for updates

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- uBlock Origin developers for the powerful filtering engine
- Community contributors who help identify problematic sellers
- Epic Games for providing the fab.com marketplace platform 