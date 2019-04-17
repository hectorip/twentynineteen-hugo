# Twenty Nineteen Hugo

This is a [Hugo](https://gohugo.io) port of WordPress's Twenty Nineteen theme.

## Highlights

- Accent color configurable via config.toml
- Featured images via `image:` in your post or page frontmatter 
- Featured image filter effect works and can be disabled
- Menu locations and social menu icons all work using Hugo's built-in menus
- Syntax highlighting included with the Monokai Light syntax theme

## Installation

From the root of your site:

`git submodule add https://github.com/jeremybise/twentynineteen-hugo.git themes/twentynineteen-hugo`

In your `config.toml`, add the following:

`theme = "twentynineteen-hugo"`

## Updating

From the root of your site:

`git submodule update --remote --merge`

## Differences from original theme

- Comment stuff has been omitted
- Author stuff has been omitted

## Content Notes

- To set a featured image for a post or page, add `image: /path/to/image.jpg` to your post or page's frontmatter.

## Available Site Params

Some theme features can be configured in `config.toml`. Here are the options:

```toml
[params]
  accent_color = "#FF0000" # Set a custom accent color for links and image filters, if enabled. Defaults to blue.
  description = "This is the site tagline." # Adds tagline next to the site title.
  privacy_link = "/privacy/" # Relative URL to privacy page, if there is one. This enables a Privacy Policy link in the footer. The link doesn't display if this isn't specified.
  disable_image_filters = false # Setting to true disables the color filter feature on images. Defaults to false.
```

## Menus

The theme includes three menu locations: `main`, `social` and `footer`.

You can include pages in the `main` and `footer` menus using any of Hugo's documented methods.

The social menu can be configured in `config.toml` using this example:

```toml
[menu]
  [[menu.social]]
    identifier = "github"
    name = "Github"
    url = "https://github.com/gohugoio"
  [menu]
  [[menu.social]]
    identifier = "twitter"
    name = "Twitter"
    url = "https://twitter.com/gohugoio"
```

The theme uses the `identifier` to determine which icon to show. For a listing of which icons are available, check out the [social icons partial folder](https://github.com/jeremybise/twentynineteen-hugo/tree/master/layouts/partials/icons/social).

## Syntax Highlighting

Add pygments config to your `config.toml`:

```toml
pygmentsUseClasses=true
pygmentsCodefences=true
```

## Google Analytics

Add your Google Analytics Tracking Code ID to your `config.toml`:

```googleAnalytics = "UA-123-45"```

The asynchronous tracking script will be included on pages on the live server, but not the dev server.

## Roadmap

- [ ] Navigation menu dropdowns
- [ ] Include search via Lunr or Fuse