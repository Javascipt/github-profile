# github-profile [![Build Status](https://travis-ci.org/Javascipt/github-profile.svg?branch=master)](https://travis-ci.org/Javascipt/github-profile)

This Repo is a fork of [github-username](https://github.com/sindresorhus/github-username), all credits should go to its author [Sindre Sorhus](https://github.com/sindresorhus).

> Get a GitHub profile from an email address


## Install

```
$ npm install github-profile
```


## Usage

```js
const githubProfile = require('github-profile');

githubProfile('sindresorhus@gmail.com').then(profile => {
    console.log(profile);
    /* => 
        {
            "login": "sindresorhus",
            "id": 170270,
            "avatar_url": "https://avatars1.githubusercontent.com/u/170270?v=4",
            "gravatar_id": "",
            "url": "https://api.github.com/users/sindresorhus",
            "html_url": "https://github.com/sindresorhus",
            "followers_url": "https://api.github.com/users/sindresorhus/followers",
            "following_url": "https://api.github.com/users/sindresorhus/following{/other_user}",
            "gists_url": "https://api.github.com/users/sindresorhus/gists{/gist_id}",
            "starred_url": "https://api.github.com/users/sindresorhus/starred{/owner}{/repo}",
            "subscriptions_url": "https://api.github.com/users/sindresorhus/subscriptions",
            "organizations_url": "https://api.github.com/users/sindresorhus/orgs",
            "repos_url": "https://api.github.com/users/sindresorhus/repos",
            "events_url": "https://api.github.com/users/sindresorhus/events{/privacy}",
            "received_events_url": "https://api.github.com/users/sindresorhus/received_events",
            "type": "User",
            "site_admin": false,
            "name": "Sindre Sorhus",
            "company": "@avajs @chalk @yeoman",
            "blog": "https://sindresorhus.com",
            "location": "° ☾ ☆ ¸. ¸　★  :.　 . • ○ ° ★",
            "email": null,
            "hireable": null,
            "bio": "Maker · Open-Sourcerer · Into Swift and Node.js",
            "public_repos": 964,
            "public_gists": 70,
            "followers": 22678,
            "following": 46,
            "created_at": "2009-12-20T22:57:02Z",
            "updated_at": "2018-02-17T04:09:43Z"
        }
    */
});
```


## API

### githubProfile(email, [token])

Returns a `Promise` for the profile.

#### email

Type: `string`

Email address for the user of whom you want the profile.

#### token

Type: `string`

GitHub [personal access token](https://github.com/settings/tokens/new).

:warning: This module may consume up to 3 API calls toward your [github rate limit](https://developer.github.com/v3/rate_limit/).

## Related

- [github-username](https://github.com/sindresorhus/github-username) - Get only username
- [github-username-cli](https://github.com/sindresorhus/github-username-cli) - CLI for github-username


## License

MIT
