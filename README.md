# Instructions

## Clone repo and install dev dependencies

```bash
git clone https://github.com/ahmedovv123/automatic-verificator-of-HTML-and-MD.git automatic-verificator
cd automatic-verificator
npm install --dev
```

## HTML Linting

We can check any .html file for any problems with command:

```bash
npx eslint yourfile.html

# If there is problems we can fix them simply by:

npx eslint yourfile.html --fix
```

## MD Linting

### Steps for installing .md linter

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

## Check commit names

Commit names are checked automaticly when we run the command

```bash
git commit -m '<type>: <subject>'
```

It is configured that type must start with lower-case and subject with start case or sentence case. You can check the file *commitlint.config.js* for more info.

Also we can check anytime manually:

```bash
echo "foo" | commitlint

⧗   input: foo
✖   subject may not be empty [subject-empty]
✖   type may not be empty [type-empty]

✖   found 2 problems, 0 warnings

####

echo "feat: add feature" | commitlint

⧗   input: feat: add feature
✖   subject must be start-case, sentence-case [subject-case]

✖   found 1 problems, 0 warnings

####

echo "feat: Add feature" | commitlint

# Passes
```
