# Services

```{contents}
:local:
```

## Bootsrap your Documentation

1. Provide a skeleton project that matches your team's requirements
2. Generate a Sphinx project based on your existing Markdown or reStructuredText documentation

## Custom Directives, Roles, and Extensions

1. [sphinx-md](https://pypi.org/project/sphinx-md/) A Sphinx extension developed specifically to turn existing Markdown documentation in a GitHub repository into a working Sphinx project within minimal impact to existing doc structure.

## Theme layout and appearance

Base your docs on the  "Read the Docs" or other theme to get started. If that doesn't meet your needs and we can tweak it to get it just the way you like.

## API documentation integration

Integrating Python docstrings into Sphinx is trivial (that's what is was made for), but it is also possible to integrate Doxygen based content into Sphinx. Here are a couple of projects that we helped:

1. [OneDNN](http://uxlfoundation.github.io/oneDNN/)
2. [OpenVINO](https://docs.openvino.ai/2025/index.html)

## Custom Output Targets

Some projects need to be published to multiple formats. Sphixn supports publishing to `html` natively, but with a little work it can publish to `docx` and `pdf` as well. Beyond that we have experience converting Sphinx based projects to the Darwin Information Typing Architecture (`DITA`) using a custom extension as well.

## Internationalization Support

Sphinx has built-in support for `.po` files, including tracking out-of-date files. We can help you get started.

## Automated build and deployment

CI/CD saves time and improves quality. We can make sure your docs are up to date by automating deployment from GitHub or integrate into your exisitng automation framework.