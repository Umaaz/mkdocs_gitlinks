# MkDocs GitLinks

A simple [MkDocs](https://www.mkdocs.org/) plugin that turns shorthand Markdown links into rich GitHub repository links with icons.

## Installation

```bash
pip install mkdocs-gitlinks
```

## Quick Start

Add the plugin to your `mkdocs.yml`:

```yaml
plugins:
  - mkdocs_gitlinks:
```

Then in your Markdown, link to any GitHub repository using:

```markdown
[github](organisation/project)
```

For example, to link to this project:

```markdown
[github](Umaaz/mkdocs_gitlinks)
```

The plugin replaces the link with a styled anchor containing the GitHub icon and repository name, linking to `https://github.com/organisation/project`.

## Configuration

All options are set under the `mkdocs_gitlinks` plugin in `mkdocs.yml`:

```yaml
plugins:
  - mkdocs_gitlinks:
      show_docs: false          # Include a link to the project's GitHub Pages site
      github_host: github.com   # GitHub hostname (change for GitHub Enterprise)
      github_docs_host: github.io  # GitHub Pages hostname suffix
      target: _blank            # Link target attribute (_blank, _self, etc.)
```

| Option | Default | Description |
|---|---|---|
| `show_docs` | `false` | When `true`, adds a secondary link to `https://<org>.github.io/<project>` with a docs icon. |
| `github_host` | `github.com` | The GitHub hostname. Override this for GitHub Enterprise instances. |
| `github_docs_host` | `github.io` | The hostname suffix used for GitHub Pages links. |
| `target` | `_blank` | The `target` attribute on generated links. |

## Example

Given this Markdown:

```markdown
- [github](intergral/deep)
- [github](intergral/deep-proto)
```

With `show_docs: true`, each item renders as a link to the GitHub repository (with a GitHub icon) alongside a link to its GitHub Pages site (with a docs icon).

## License

Apache-2.0
