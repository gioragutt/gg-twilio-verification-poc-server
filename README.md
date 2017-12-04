# This is POC of using the twilio API

See `.env.example` for required environment variables

## Usage

run server with `npm start`

## Example messages

```sh
curl --request POST \
  --url http://localhost:3000/api/v1/sendCode \
  --header 'content-type: application/json' \
  --data '{
	"phone": "Y0UR4H0N3",
	"countryCode": "972"
}'
```

*wait for sms here*

```sh
curl --request POST \
  --url http://localhost:3000/api/v1/verifyCode \
  --header 'content-type: application/json' \
  --data '{
	"phone": "Y0UR4H0N3",
	"countryCode": "972"
	"code": "CODE FROM SMS HERE!"
}'
```
