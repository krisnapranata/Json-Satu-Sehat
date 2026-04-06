# Json-Satu-Sehat

cara menjalankan :

ganti :
client_id satu sehat
clent_secret satu sehat


curl --insecure --location \
  --header 'Content-Type: application/x-www-form-urlencoded' \
  --data-urlencode 'client_id=<CLIENT_ID> ganti ya' \
  --data-urlencode 'client_secret=<CLIENT SECRET SATU SEHAT> ganti' \
  --request POST \
  'https://api-satusehat.kemkes.go.id/oauth2/v1/accesstoken?grant_type=client_credentials'

  1. dapat access_token
  2. ganti curl dibawah ini dengan acces_token yang didapat
  3. ganti nama @medication.json sesuai dengan nama2 json dalam 1 folder yang sama


curl -X POST "https://api-satusehat.kemkes.go.id/fhir-r4/v1/Medication" \
 -H "Authorization: Bearer <acces_token>" \
 -H "Content-Type: application/json" \
 -d @medication.json