# MD Linting

## Steps for installing .md linter

*repo:* [Markdown lint tool](https://github.com/markdownlint/markdownlint)

First we need Ruby installed on local machine:

```bash
sudo apt update
sudo apt install ruby-full
# Verify the install
ruby --version
```

Next install the tool through [rubygems](https://rubygems.org/):

```bash
gem install mdl
# Then we can lint .md files with command:
mdl README.md
# or directories with command:
mdl docs/
```
