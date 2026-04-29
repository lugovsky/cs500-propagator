# cs500-propagator

GitHub Pages redirect for the CS500 mobile browser.

Mobile visitors are redirected into Expo Go with the latest published `projects/browser` OTA update.
Desktop visitors are redirected straight to the original `url` query parameter.

## Update flow

1. Publish the browser OTA update from `cs500-price-scraper` with `cd projects/browser && npx eas-cli update --branch preview --message "..."`
2. Copy the new EAS update group ID from the CLI output.
3. Update `LATEST_EXPO_GROUP_ID` in `index.html`.
4. Commit and push this repo so GitHub Pages serves the new redirect target.
