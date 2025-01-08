# Galv website

The website is built on top of the [Docsy Example Project](https://github.com/google/docsy-example) for [Hugo](https://gohugo.io).

## Running the website

You can run the docs inside a [Docker](https://docs.docker.com/) container, the container runs with a volume bound to the root directory.
This approach doesn't require you to install any dependencies other than [Docker Desktop](https://www.docker.com/products/docker-desktop) on Windows and Mac, and [Docker Compose](https://docs.docker.com/compose/install/) on Linux.

To run, use `docker-compose up` from the root of the project. 
It will build the image and start the container, then you can access the website at `http://localhost:1313`.
Note: If user gets a `permission denied` type of error, it is suggested to change the permissions on the directory to read/write/execute state. Alternatively, in `docker-compose.yaml` file, change the launch command to `server --poll 700ms --bind 0.0.0.0 --noBuildLock`.

The container will watch for changes in the files and automatically rebuild the site.
To support Windows (WSL), we use polling (`--poll 700ms`) to watch for changes rather than the default filesystem watcher.

## Hugo/Docsy QuickStart:

### Content structure

The content of the site is in the `content/xx` directory, where `xx` is the language code (e.g., `en` for English).
The content is written in Markdown format with Hugo front matter and code snippets.

Each major page of the site has a directory in the `content/xx` directory with an `_index.md` or `index.md` file that defines the content for that page.
The `_index.md` file is used for the main page content (i.e. `content/xx/_index.md`), and `index.md` is used for the content of the subpages (e.g. `content/xx/about/index.md`).
Resources that pages need are kept at the same level as the page's markdown file.

Within major pages you can also create subpages either by creating a directory with an `index.md` file or by creating a markdown file (with any name you like).
The page's URL is determined by the directory structure and the file name, so the url `about/contact/` will have its markdown file as `content/xx/about/contact/index.md` or `content/xx/about/contact.md`.

### Using shortcodes

Most of the content is structured by Docsy shortcodes (or uses Hugo shortcodes). 
These appear within Hugo tags like `{{% shortcode %}}` or `{{< shortcode >}}`.

A list of available shortcodes can be found in the [Docsy documentation](https://www.docsy.dev/docs/adding-content/shortcodes/) and in the [Hugo documentation](https://gohugo.io/content-management/shortcodes/).

#### `{{%` vs `{{<`

The `{{%` syntax is used for shortcodes that wrap content that requires additional processing (i.e. content written in Markdown). 
The `{{<` syntax is used when you do not want the content to be processed (i.e. content written in HTML).
In practice, you'll probably want to use `{{%` most of the time.
