# dab-clocky

## GitHub Action Note

The GitHub Action will fail after pushing the code because `Login to Azure` requires permissions on a registered application in Entra ID.

Make sure the service principal or registered app has the required API permissions and consent before the workflow runs.
