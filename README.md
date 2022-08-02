# friendly-carnival-template
Template geral

## New
Testing auto CHANGELOG.md

https://medium.com/jobtome-engineering/how-to-generate-changelog-using-conventional-commits-10be40f5826c
https://youtu.be/2J9VnYiZ_Ts

Test yarn init postinstall script!

```sh
yarn add --dev @commitlint/{config-conventional,cli} husky standard-version
yarn husky install
yarn husky add .husky/commit-msg 'yarn commitlint --edit $1'
```
```json
# package.json
{
  "scripts": {
    "postinstall": "husky install",
    "release": "standard-version && git push --follow-tags origin $(git branch --show-current)"
  }
}
```
```json
# .commitlintrc.json
{
  "extends": ["@commitlint/config-conventional"]
}
```