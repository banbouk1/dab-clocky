# dab-clocky

## Get a token (client secret)
curl -X POST -H "Content-Type: application/x-www-form-urlencoded" https://login.microsoftonline.com/TENTANT_ID_GOES_HERE/oauth2/v2.0/token -d 'client_id=XXX' -d 'client_secret=XXX' -d 'grant_type=client_credentials' -d 'scope=api://XXX/.default' 

## Make a REST API request
curl -X 'GET' 'http://acaname.randomname.region.azurecontainerapps.io/api/ViewSAP' -H 'accept: application/json' -i --header 'X-MS-API-ROLE: dab.reader' --header 'Authorization: Bearer TOKEN_GOES_HERE'

## GitHub Action Note

The GitHub Action will fail after pushing the code because `Login to Azure` requires permissions on a registered application in Entra ID.

Make sure the service principal or registered app has the required API permissions and consent before the workflow runs.

