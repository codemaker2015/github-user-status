<h3 align="center">GitHub User Status CLI</h3>
<p align="center">A CLI for setting your GitHub user status<p>

## Usage

You'll need to [set a GitHub personal access token](https://help.github.com/en/articles/creating-a-personal-access-token-for-the-command-line) to `GITHUB_TOKEN`, with the `user` scope if you want to change your own status. You can also use the `-t=<token>` flag.

### Get your own status

```sh
$ npx github-user-status
```

With a GitHub personal access token:

```sh
$ npx github-user-status -t <token>
```

### Get the status of a user

```sh
$ npx github-user-status -u <user>
```

### Change your status

```sh
$ npx github-user-status -m <message> -e [emoji]
```

## Programmatic Usage

```js
const { getUserStatus, changeUserStatus } = require('github-user-status')

// Get your own status
getUserStatus(token)

// Get a user's status
getUserStatus(token, 'Codemaker')

// Set your status
changeUserStatus(
  {
    message, // string, required
    emoji, // string
    expiresAt, // string
    limitedAvailability, // boolean
  },
  token
)
```
