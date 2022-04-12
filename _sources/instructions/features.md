# Jupyter Book Features

You can find the complete documentation
[here](https://jupyterbook.org/intro.html). Bellow some of my favourite features.

## Some possible cards

See more [here](https://jupyterbook.org/content/content-blocks.html).

:::{note}
Create notes card
:::

:::{warning}
Create warnings card
:::

:::{admonition} Add title!
Create admonition card
:::

:::{tip}
Create tip card
:::

:::{seealso}
Create see more card
:::

:::{dropdown} Add title!
Create dropdown card
:::

### Add code blocks

```python
print('hello world')
```

```bash
$ cd ~
```

### Combine elements

:::{dropdown} See my python code

```python
print('hello world')
```

:::

## Glossary

See the Jupyter Book Glossary documentation
[here](https://jupyterbook.org/content/content-blocks.html?highlight=glossary#glossaries).

See this glossary example:

```{glossary}
changeset
    A group of changes to one or more files that are or will be added
    to a single {term}`commit` in a version control
    repository.

commit
    To record the current state of a set of files (a {term}`changeset`)
    in a version control repository. As a noun,
    the result of committing, i.e. a recorded changeset in a repository.
    If a commit contains changes to multiple files,
    all of the changes are recorded together.

conflict
    A change made by one user of a version control system
    that is incompatible with changes made by other users.
    Helping users resolve conflicts
    is one of version control's major tasks.

HTTP
    The Hypertext Transfer Protocol used for sharing web pages and other data
    on the World Wide Web.
```

## Citations and bibliographies

See the Jupyter Book citation and bibliography documentation 
[here](https://jupyterbook.org/tutorials/references.html?highlight=bibliography).

### Citations

- The citation {cite:p}`holdgraf_evidence_2014`
- The citation {cite:t}`holdgraf_rapid_2016`
- The citation {cite:ps}`holdgraf_portable_2017`
- The citation {cite:ts}`holdgraf_encoding_2017`

### Bibliography

```{bibliography}
:style: unsrt
```