# Violation Comments Action

This is a [GitHub action](https://docs.github.com/en/actions/creating-actions/about-custom-actions) to help using [Violation Comments To GitHub Command Line
](https://github.com/tomasbjerre/violation-comments-to-github-command-line). 

## Usage

Example:

```yml
jobs:
  call-workflow:
    uses: tomasbjerre/.github/.github/workflows/gradle-ci.yml@master
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Violation Comments Action
        uses: tomasbjerre/violation-comments-action@v1-pre
        with:
          accesstoken: asdasdas # use a secret!
          parser: CHECKSTYLE
          regexp: '.*checkstyle/main\.xml$'
```
