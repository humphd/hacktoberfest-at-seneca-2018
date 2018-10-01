# Data

The `data/` directory contains various files for tracking and submission of
student contributions to Hacktoberfest 2018/Release 0.2.

Make sure to run `npm install` before you alter these files so that
[prettier gets run when you stage your files](https://github.com/humphd/hacktoberfest-at-seneca-2018/pull/11).

**NOTE: submit Pull Requests for any changes you want to make to the files mentioned below. Every Pull Request must be reviewed and approved by another student before it can be merged.**

## people.json

An `Array` of GitHub usernames for students in DPS909 and OSD600
participating in Hacktoberfest. This list is used to generate and
reference other data below.

_If your username is missing, or incorrect, please send a PR to fix it._

## posts.json

An `Object` containing blog post URLs (`String`) and date (`YYYY-MM-DD` as a `String`)
posted grouped by GitHub username. As you write posts about your work, please
update this file with relevant links. The format is as follows:

```json
"username": [
    {
        "url": "http://blog.com/first-blog-post",
        "date": "2018-10-03"
    },
    {
        "url": "http://blog.com/second-blog-post",
        "date": "2018-10-04"
    }
],
"username2": [
    {
        "url": "http://username2.blogspot.com/fixing-a-bug",
        "date": "2018-10-05"
    }
]
```

## issues.json

An `Object` containing info about GitHub Issues being worked on, or which
have been completed, grouped by GitHub username. As you begin working on
bugs, please record the info here. The format is as follows:

```js
"username": [
    {
        "repo": "filerjs/filer",
        "number": 123,
        "started": "2018-10-11"
    },
    {
        "repo": "Microsoft/vscode",
        "number": 1235,
        "started": "2018-10-01"
    }
]
```

In the example above, `username` is working on two Issues:

1. https://github.com/filerjs/filer/issues/123
2. https://github.com/Microsoft/vscode/issues/1235

The `repo` is the portion of the GitHub URL that comes after `github.com`:
`https://github.com/{owner}/{name}`. The `number` is the Issue number. The `started`
property is the date (`YYYY-MM-DD` as a `String`) the user started working on this
issue.

> NOTE: make sure you have left a comment in any Issue you want to work on, and have been given the go-ahead from the project to fix it before you add it to this file.

## pull-requests.json

An `Object` containing info about GitHub Pull Requests being worked on,
or which have been completed, grouped by GitHub username. When you submit a
Pull Request, please record the info here. The format is as follows:

```js
"username": [
    {
        "repo": "filerjs/filer",
        "number": 300,
        "started": "2018-10-01"
    },
    {
        "repo": "Microsoft/vscode",
        "number": 3200,
        "started": "2018-10-01",
        "merged": "2018-10-20"
    }
]
```

In the example above, `username` is working on two Pull Requests:

1. https://github.com/filerjs/filer/pull/300
2. https://github.com/Microsoft/vscode/pull/3200

The `repo` is the portion of the GitHub URL that comes after `github.com`:
`https://github.com/{owner}/{name}`. The `number` is the Pull Request number.
The `started` property is the date (`YYYY-MM-DD` as a `String`) the user started
working on this pull request.

When your Pull Request is merged (and only if it gets merged), add the `merged`
date (`YYYY-MM-DD` as a `String`). If `merged` is not present, it is assumed that
the Pull Request is not merged (yet). Make sure you add `merged` whenever you
complete a Pull Request for Hacktoberfest, to indicate that you have completed
one of your requirements.

> NOTE: it's possible that a Pull Request will NOT get merged for one reason or another. This is outside your control, and you should still record your Pull Requests here, even if they never get merged.
