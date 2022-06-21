# Upload Shpinx HTML documentation to Orfium's docs repository

## Description
This Github Action pushes your project documentation into Orfium's repository that centralize all projects documentation.

## Inputs
1. The docs repository where you want to deploy your project's documentation
2. The deploy key
3. A user email having the rights to commit in the docs repo. Default value: "github-service-account@orfium.com"
4. The user name. Default value: "orfium-orf"

## Usage
Add this to your CI with your values in the inputs:

      - name: Upload with documentation action
        uses: Orfium/upload-sphinx-html-orfium-docs@master
        with:
          deploy_key: ${{ secrets.DOCS_DEPLOY_KEY }}
          docs_repo: Orfium/docs
