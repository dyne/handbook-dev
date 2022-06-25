# Create and manage a staging environment

So we need to have a staging environment for our softwares written in node.js
here will share our experience on how better move within the messy .js world.

## Ingredients

- Some application server, [pm2](https://pm2.keymetrics.io/)
- Some proxy to handle ssl and dns addresses, [Greenlock proxy](https://github.com/Roslovets-Inc/greenlock-proxy)
- A easy way to do Continous Delpoyment, [Github Actions](https://github.com/dyne/deploy-node-pm2)

## Receipe

1. Grab a [Devuan](https://devuan.org) 💫 machine
1. Install node environment [see here](/devops/node_install.md)
1. Install the `pm2` as a global command
1. Install the proxy software🦄
1. Configure the github action on your repository
1. Push edits and see the magic 🪄
