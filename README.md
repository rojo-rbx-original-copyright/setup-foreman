# Setup Foreman GitHub Action
GitHub Action to install [Foreman](https://github.com/rojo-rbx/foreman), a toolchain manager primarily intended for Roblox projects.

This action will install a release version of Foreman and run `foreman install` from the root of your project. This ensures any tools specified in your project's `foreman.toml` file will be available to the rest of the workflow!

## Usage
Add a step to your workflow file:

```yaml
- uses: rojo-rbx/setup-foreman@v1
  with:
    token: ${{ secrets.GITHUB_TOKEN }}
```

### Action Parameters

#### `token` (required)
A GitHub token used to interact with the GitHub API. This is used for installing Foreman itself, and then passed to Foreman to install other tools from GitHub.

#### `version` (optional)
A SemVer version range of Foreman to install.

If not specified, the latest stable release will be installed.

## License
setup-foreman is available under the MIT license. See [LICENSE.txt](LICENSE.txt) or <https://opensource.org/licenses/MIT> for details.