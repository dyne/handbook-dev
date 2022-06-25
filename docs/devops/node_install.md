# Best way to install node

We assume we are talking about [Devuan 💫](https://devuan.org).

The easiests, fastest and more proficient way is to use
[`nvm`](https://github.com/nvm-sh/nvm)

Please proceed with:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/master/install.sh | bash
source ~/.bashrc
nvm install node
```

## Useful tools

When working together with node.js we often use package managers other that
`npm` like `yarn` and `pnpm` please install them as your wish, since many times
they are referenced in our projects

```bash
npm install --global yarn
curl -fsSL https://get.pnpm.io/install.sh | sh -
```
