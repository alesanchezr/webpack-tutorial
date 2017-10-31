# WARNING! Before beginning with this steps, make sure you have already completed the steps in the README's "master" branch.

## Configuring webpack for WordPress

The biggest change in a Webpack WordPress Installation is that you have to specify the dist or public directoy inside the active theme.
Also, WordPress required jQuery and a separate Styles.css file that includes the commentaries describing the theme (event if the CSS file is uglified/compressed).
