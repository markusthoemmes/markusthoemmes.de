# markusthoemmes.de

This repository contains my personal "website". It is hosted on **Github Pages** :rocket:.

## Installation

Well, not much to do here, just a veeery lightweight build process to optimize images.

Install ImageOptim:

```
brew cask install imageoptim
npm install -g imageoptim
```

**Bonus:** Setup a pre-commit hook to optimize images

```
echo 'images=$(git diff --exit-code --cached --name-only --diff-filter=ACM -- "*.png" "*.jpg")
$(exit $?) || (echo "$images" | imageoptim && git add $images)' > .git/hooks/pre-commit
```