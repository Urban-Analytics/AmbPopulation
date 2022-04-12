# General workflow

First you should clone the GitHub repository:

```bash
$ git clone https://github.com/Urban-Analytics/AmbPopulation.git
```

Enter the book folder

```bash
cd book
```

Then you can use markdown files to documenting the project content.

:::{note}
There is no rules about how you should organize the markdown files,
but I strongly recommend organizing the content into folders and subfolders
(see part1 and part2 examples).
:::

## `_toc.yml` file

After write some markdown documents, we need to specify how they should be
organized in our book. To do this, we use the `_toc.yml` file. See an example
bellow:

```yaml
# Table of contents
# Learn more at https://jupyterbook.org/customize/toc.html

format: jb-book
root: intro
parts:
- caption: Part 1 title
  chapters:
  - file: part1/overview
    sections:
    - file: part1/session1
    - file: part1/session2
```

The `home` page is set under `root` flag - in this case, our home page is going
to be build using the `intro.md` file.

The structure can be divided in parts, chapters and sections. For every content
you need to add the file path (without the `.md`).

## `_config.yml` file

All configuration parameters are organized under the `_config.yml` file.
Some parameters includes:

- title
- author
- email
- logo path
- url
- htlm related parameters

## Building the book

### Working with this project locally

To build the book locally, you need install Jupyter Book (see instructions
[here](https://jupyterbook.org/start/overview.html)), and then run the following
command:

```bash
# navigate to the repository root
$ cd AmbPopulation
# sometimes worth running jupyter-book clean book/ to remove old files
$ jupyter-book build book/
```

The book is automaticity rendered with Jupyter Book and all html files and
related files are stored inside `book/_build/` folder. You can then navigate in
the `book/_build/` and open the `index.html` file to locally visualize the book.

:::{note}
This step is optional, once the GitHub can perform this step every time that
new content is added to `main` branch.

However, this step is recommended, once is a good practice to review local
changes before committing to GitHub.
:::

:::{note}
The `_build` folder is just a local folder, once the `.gitignore` prevent this
folder to be pushed to GitHub.
:::

### Working with this project on GitHub

After write some markdown files and add then to `_toc.yml` file you can `push`
your changes to `GitHub`. You should do this using a secondary branch, so:

```bash
$ git checkout -b newBranchName
$ git add .
$ git commit -m "commit message"
$ git push origin newBranchName
```

Then go to the GitHub and do a Pull Request - be sure to request at least
one reviewer.

Once the Pull Request is approved, the new content is going to be merged with
the `main` branch and will trigger the GitHub Action configured by the
`.github/workflows/buildbook.yml` file.

The `buildbook` action will build the book and store the `_build` files in a
different branch (`gh-pages`). This will keep the main branch as clean as
possible as well as prevent us from break any file related with the _build
folder.
