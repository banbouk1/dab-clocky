# dab-clocky

## Get a token (client secret)
curl -X POST -H "Content-Type: application/x-www-form-urlencoded" https://login.microsoftonline.com/1a92b2d4-5d6a-4db0-bc17-0f3feaa5e771/oauth2/v2.0/token -d 'client_id=90ce22e2-25a1-4114-839d-20a438a514e1' -d 'client_secret=r.B8Q~bbEsx3iPNZKEy5sY5jwoLqnx3PeqoIjcKr' -d 'grant_type=client_credentials' -d 'scope=api://d71a3962-bc8a-49ea-9200-fbce350172a0/.default' 

## Make a REST API request
curl -X 'GET' 'http://acaname.randomname.region.azurecontainerapps.io/api/ViewSAP' -H 'accept: application/json' -i --header 'X-MS-API-ROLE: dab.reader' --header 'Authorization: Bearer TOKEN_GOES_HERE'

## GitHub Action Note

The GitHub Action will fail after pushing the code because `Login to Azure` requires permissions on a registered application in Entra ID.

Make sure the service principal or registered app has the required API permissions and consent before the workflow runs.

