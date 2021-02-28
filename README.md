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

## Specifying folder path
You can specify an optional folder path to search for AssemblyInfo.cs or AssemblyInfo.vb files. The default value is ${{ github.workspace }}

```yml
- name: Set version on AssemblyInfo.cs
  uses: dannevesdantas/set-version-assemblyinfo-win@v0.1.4
  with:
    version: '3.2.0'
    path: '${{ github.workspace }}/MyProject/App'
```

## Requirements
This GitHub Action is compatible with Windows based runners only. If you are looking for a Linux based version, please visit [sonatype-nexus-community/nexus-repo-github-action](https://github.com/sonatype-nexus-community/nexus-repo-github-action).

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)
