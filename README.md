> :warning: This CSS Stylesheet is not used in the current BookMonkey Versions (2-4) from the "Angular Buch". 

# book-monkey-styles

This repository contains the global stylesheet to be used within the example application "BookMonkey" used in the German [Angular Book](https://angular.buch.com).

## Usage

Install the NPM package from the registry:

```bash
npm i --save book-monkey-styles
```

Then you can include the stylesheet in the Angular build process using via the `angular.json` config file:

```json
{
  /* ... */
  "projects": {
    "book-monkey": {
      /* ... */
      "architect": {
        "build": {
          /* ... */
          "options": {
            /* ... */
            "styles": [
              "src/styles.css",
              "node_modules/book-monkey-styles/styles.css"
            ],
            /* ... */
          },
          /* ... */
        },
        /* ... */
        "test": {
          /* ... */
          "options": {
            /* ... */
            "styles": [
              "src/styles.css",
              "node_modules/book-monkey-styles/styles.css"
            ],
            /* ... */
          }
        },
        /* ... */
      }
    }
  },
  /* ... */
}
```

Alternatively you can import the CSS file via `include` in your `styles.css` file:

```css
@import '~book-monkey-styles/styles.css';
```