When you create a new repo with this template, you should update the files in this directory.

In `dependabot.yml`, remove the ecosystems your app is missing. For example, if it only has a Python function, it should be as follows:

```yaml
version: 2
updates:
  - package-ecosystem: pip
    directory: "/functions/path-to-your-function/"
    schedule:
      interval: weekly
  - package-ecosystem: github-actions
    directory: "/"
    schedule:
      interval: weekly
```

In the workflows directory, create a `main.yml` that resembles one of the other samples:

- **foundry-sample-mitre**: [`main.yml`](https://github.com/CrowdStrike/foundry-sample-mitre/blob/main/.github/workflows/main.yml) to build extensions and pages with Yarn. It also has a [`rebuild.yml`](https://github.com/CrowdStrike/foundry-sample-mitre/blob/main/.github/workflows/rebuild.yml) to rebuild the UI bits with the latest dependencies every week. 
- **foundry-sample-rapid-response**: [`main.yml`](https://github.com/CrowdStrike/foundry-sample-rapid-response/blob/main/.github/workflows/main.yml) to compile Go functions and build/test UI pages.
- **foundry-sample-ngsiem-importer**: [`main.yml`](https://github.com/CrowdStrike/foundry-sample-ngsiem-importer/blob/main/.github/workflows/main.yml) to install Python dependencies, run unit tests, and confirm the function starts successfully. 

Once you've completed these updates, please delete this file.
