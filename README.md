# Github Action to deploy to Dropbox

## Configuration

Follow [this guide](https://preventdirectaccess.com/docs/create-app-key-access-token-for-dropbox-account/#access-token) to create and get your access token

Save the token to your repository `Settings > Secrets`:

- Name: `DROPBOX_ACCESS_TOKEN`
- Value: `YOUR_TOKEN`

## Github workflow file


```yml
- uses: intersecato/dropbox-upload@v1.0.0
    with:
      DROPBOX_ACCESS_TOKEN: ${{ secrets.DROPBOX_ACCESS_TOKEN }}
      DROPBOX_DESTINATION_PATH_PREFIX: "folder path"
      GLOB: "file path"
```
