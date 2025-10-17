# Workflow-Templates
Collection of useful workflow templates

To call a template, create a new workflow template with the following (replace csproj_path value with the csproj file to be built and published as a nuget package and dotnet-pack-template.yml with the workflow template to use if different):

name: MyTemplateName

on:
  workflow_dispatch:

jobs:
  call-template:
    uses: zerihal/github-actions-templates/.github/workflow-templates/dotnet-pack-template.yml@main
    with:
      csproj_path: './MyLibrary/MyLibrary.csproj'
      dotnet_version: '9.0.x'
