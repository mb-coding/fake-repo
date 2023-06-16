# Contributing

## 1. Navigating the Repository

First, open the [github repository](https://github.com/nerdherd/documentation) in a web browser.

Your account must be a part of the [nerdherd Github organization](https://github.com/nerdherd) 
in order to edit the repository.
To be invited, please contact a programming subteam member.

Then, click on the [`source` folder](https://github.com/nerdherd/Documentation/tree/main/source) to see the markdown files for each page.

### 5. Adding Images

To add an image, first upload an image in the [`/source/images` directory](https://github.com/nerdherd/Documentation/tree/main/source/images).

Then, to embed the image in a document, add:

```md
![Alternate Text](./images/IMAGE_NAME)

*Add a caption here*
```

or

:::md

```{image} ./images/IMAGE_NAME

```

*Add a caption here*

:::

You can change the image's size and other properties by doing:

:::md

```{image} ./images/IMAGE_NAME
:alt: ALTERNATE IMAGE TEXT
:width: 200px
:align: left
```

:::

For more information, see the [MyST Parser](https://myst-parser.readthedocs.io/en/latest/syntax/optional.html#html-images) documentation.

## Adding New Pages

To add a new page, create a markdown file for it in the `source` [folder](https://github.com/nerdherd/Documentation/tree/main/source).

Then, add it to the table of contents in [index.rst](https://github.com/nerdherd/Documentation/tree/main/source/index.rst) for it to appear on the website.

```rst
.. toctree::
   :maxdepth: 1
   :caption: About:

   PAGE NAME <./PAGE_FILE.md>
   PAGE 2 NAME <./PAGE_2_FILE.md>
```

Make sure that there is an empty line between the `:caption:` line and the first page name.

You can add additional `toctree`s to add more sections on the sidebar.

