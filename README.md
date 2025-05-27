# fabfilter - uBlock Origin Filter for fab.com

A simple uBlock Origin filter to block specific creators and assets on fab.com (Epic Games' digital content marketplace).

## What This Filter Does

This filter provides a simple way to:
1. **Block specific creators by name** - Hide all assets from creators you want to avoid
2. **Block specific assets by listing ID** - Hide individual problematic assets

## Installation

Filter URL: https://raw.githubusercontent.com/KiaArmani/fabfilter/refs/heads/main/fabfilter.txt

### Method 1: Direct Filter Import
1. Install uBlock Origin browser extension
2. Open uBlock Origin dashboard
3. Go to "Filter lists" tab
4. Click "Import" and add the filter URL or paste the filter content (all the way on the bottom)
5. Apply changes

### Method 2: Manual Installation
1. Copy the contents of `fabfilter.txt`
2. Open uBlock Origin dashboard
3. Go to "My filters" tab
4. Paste the filter rules
5. Apply changes

### Method 3: Browser Extension (Chrome only)

TBD

### Example Rules
```
! Block a creator named "Bad Actor"
fab.com##.fabkit-Stack-root:has(> .fabkit-Thumbnail-root):has(a[href*="/sellers/Bad%20Actor"])

! Block a specific asset 
fab.com##.fabkit-Stack-root:has(> .fabkit-Thumbnail-root):has(a[href*="/listings/61709449-01ea-4d55-9051-7f8f68dd1f1d"])
```

## Contribute

### Identifying Problematic Sellers
1. Browse fab.com normally
2. When you encounter suspicious content, note the seller information
3. Create a new issue or pull request in this repository.
4. Report the seller to Epic Games / Fab if you find them violating platform rules.

### Reporting False Positives
If legitimate content is being blocked:
1. Check the seller against the list
2. Review the keyword filters for overly broad terms
3. Submit an issue with details about the false positive

### Reporting Issues
1. Provide the specific URL where the issue occurs
2. Include screenshots if possible
3. Describe the expected vs actual behavior
4. Include your browser and uBlock Origin version

## Disclaimer

- This filter is not affiliated with Epic Games or fab.com
- Blocking decisions are based on community feedback
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
- [OGA]("http://opengameart.org/content/dungeon-crawl-32x32-tiles") for the shield icon