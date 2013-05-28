# Directory Structure

With Section the hierarchy of your site’s files is important. It is solely responsible for the resulting permalink structure.

Let’s look at an example site structure:

```text
.
├─ content
│  ├─ index.md
│  ├─ about.md
│  ├─ blog
│  │  ├─ index.md
│  │  ├─ 2013-05-20-why-section
│  │  │  ├─ index.md
│  │  │  └─ image.png
│  │  └─ 2013-04-22-reasons-to-learn-javascript.md
│  └─ docs
│     └─ overview.md
├─ assets
│  ├─ favicon.ico
│  └─ robots.txt
├─ output
├─ layout.jst
├─ style.scss
└─ config.yaml
```

Now let’s see what each of the files and directories are.


### `content`

This directory holds your content which usually means markdown files. The way files are organized here will determine the URL or permalink of each page of your site. For example the file stored in `content/docs/overview.md` will have `/docs/overview/` as the URL.

For documents where the published date is needed, such as blog posts, you can prefix the year, month and day to the name of the file. Thus the file at `site/blog/2013-04-22-reasons-to-learn-javascript.md` will have the permalink `/blog/reasons-to-learn-javascript/` and the date will be available inside the layout template.

If a document has associated files like images they can be stored along side it and will be copied over to the output directory unmodified.

__You need nothing more than this directory to generate a beautiful website.__


### `assets`

Files in this directory will be copied unmodified to the generated site. This is where you would put your static resources, such as images, scripts and stylesheets.


### `output`

This is the directory that by default holds the generated site, ready to be deployed.


### `layout.jst`

This is an optional [underscore template](http://underscorejs.org/#template) file that is used against every markdown file to generate the corresponding HTML file.


### `style.scss`

This is an optional custom stylesheet that is feeded to the [SASS](http://sass-lang.com/) CSS pre-processor. Other than `.scss` it can have `.sass` or `.css` as the extension.


### `config.yaml`

Holds configuration data as YAML or JSON—in which case a `.json` extension is needed.
