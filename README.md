# discord-accept-bot
A simple bot for people to be able to accept rules by doing `/accept`
## Running locally
### Installing globally
```sh
yarn global add discord-accept-bot
```
#### Configuring in the command line
```sh
acceptbot --prefix=! # Optional
acceptbot       -p ! # Default: /

acceptbot --command=agree # Optional
acceptbot        -d agree # Default: accept

acceptbot --channel=welcome # Optional
acceptbot        -h welcome # Default: Rules

acceptbot --role=12345678 # Required
acceptbot     -r 12345678

acceptbot --token=$TOKEN # Required
acceptbot      -t $TOKEN
```

### Cloning from the git repository
```sh
git clone git@github.com:MegaCode18/discord-accept-bot.git
cd discord-accept-bot
yarn
yarn start
```
#### Configuring from the git repository
All configuration is stored in a `.config.js` file. Here is an example of such a file:
```js
module.exports = accept => {
  accept.setPrefix('!') // Prefix to use | Default: /
  accept.setCommand('agree') // Command to use | Default: accept
  accept.setChannel('welcome') // Channel members need to use to accept | Default: #rules
  accept.setRole('123467890987654321') // Role ID to assign once rules are accepted
  accept.login('abcdefg.ABCDEFG.1234567') // Login token
}
```
