# Publish components to Nexus Repository GitHub Action for Windows based runners
Publish components to Nexus Repository.

## Usage

```yml
- name: Set version on AssemblyInfo.cs
  uses: dannevesdantas/set-version-assemblyinfo-win@v0.1.4
  with:
    version: '3.2.0'
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
This GitHub Action is compatible with Windows based runners only.

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)
