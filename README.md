# Publish artifacts to Nexus Repository GitHub Action for Windows based runners
Publish artifacts to Nexus Repository.

## Usage

```yml
- name: Publish to Nexus
  uses: dannevesdantas/nexus-publisher-win@v0.1.1
  with:
    uri: 'http://nexus.mycompany.com/repository/team/my-app/my-app/3.2.0/my-app-3.2.0.zip'
    username: ${{ secrets.NEXUS_USERNAME }}
    password: ${{ secrets.NEXUS_PASSWORD }}
    filename: '${{ github.workspace }}\my-app.zip'
```

> If a file with the same name already exists at the provided uri, it will be overwritten.

## Requirements
This GitHub Action is compatible with Windows based runners only. If you are looking for a Linux based version, please visit [sonatype-nexus-community/nexus-repo-github-action](https://github.com/sonatype-nexus-community/nexus-repo-github-action).

## Troubleshooting
If you receive an `Invoke-WebRequest : The response content cannot be parsed because the Internet Explorer engine is not available` error message, make sure you've opened Internet Explorer at least once in the runner's machine, and dismissed the run-once pop-up. For more details, please visit [Solving the First-Launch Configuration Error with PowerShell’s Invoke-WebRequest Cmdlet](https://wahlnetwork.com/2015/11/17/solving-the-first-launch-configuration-error-with-powershells-invoke-webrequest-cmdlet/).

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)
