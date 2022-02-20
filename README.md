# ticker-html

Generate HTML based ticker Browser Sources.

## Input

Performer data goes into `data.js` with up to 3 lines per performer.

HTML is permitted inside of a line so long as you use double-quotes on the outside and only single-quotes on the inside for the HTML elements.

## Formatting

CSS styles for the lines are in `ticker.html`. Modify the classes `line1`, `line2`, and `line3` as you desire.

In the included sample, the `<link>` entry at the top also loads the Didact Gothic font from Google Fonts.

You can open `ticker.html` in a browser and refresh as you update the styling to see the effects.

As you edit the styling, also edit the `width` and `height` values of the `entry` class to ensure that your style fits within the pixel bounds you desire.

When you are done, reload one last time and open your browser's Console output (usually a tab in the Inspector).
The recommended OBS Browser source height and width will be shown in the console log. The height will vary depending on the number of entries in
`data.js`, so make sure to check this every time you modify the performer data there (especially if you add performers, the height will need to increase).

## OBS Settings

The browser source width and height should be set to the recommended computed value from the Console output as described above.

The vertical distance for the move animation should be set to the entry height.

## Multiple Stylings

The performer data is separated into `data.js` so that if you need multiple stylings, you can make copies of `ticker.html` and have them all refer to the same `data.js`.

If there are some stylings that don't need all of the lines, you can add `display: none;` to the CSS class of a line.
