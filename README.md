Ping-GitHub-stale-PRs
=======

A tiny bash shell script for any GitHub repository having too many pull reuqests that can't manually check and ping the stale PRs.

## Dependencies

- curl
- grep
- awk
- sed
- [jq](https://stedolan.github.io/jq/)
- xargs
- date

## Usage

There are some variables inside `ping-stale-PRs` that you can manipulate:

- GITHUB_TOKEN         # Your [GitHub token](https://github.com/settings/tokens/new?scopes=repo&description=For%20Ping-GitHub-stale-PRs)
- OWNER                # The repository owner GitHub ID
- REPO                 # The repository name
- STALE_DAYS           # How many days a pull request stale would be pinged, `14` by default
- COMMENT              # The comment in json format (`'{"body": "Comment here please"}'`), [ref](https://developer.github.com/v3/issues/comments/#create-a-comment)

You can directly assign/oeverride value to the varible like this(Don't forget COMMENT need to be in the json format with "body" kay/value):

```sh
GITHUB_TOKEN=21eb588cda61aa8525421857eca221ef371e4109
```

To run the script, set repository name and repository owner and your [GitHub token](https://github.com/settings/tokens/new?scopes=repo&description=For%20Ping-GitHub-stale-PRs) in the executable file or the environment, take https://github.com/cdnjs/cdnjs as example:

```sh
REPO=cdnjs OWNER=cdnjs GITHUB_TOKEN=21eb588cda61aa8525421857eca221ef371e4109 ./ping-stale-PRs
```

## License

GNU General Public License v3.0

See [LICENSE](LICENSE) file for the detail
