node_modules\.bin\tsc

C:\Users\wojtalam\AppData\Roaming\npm\pm2 start pm2/xapi.json

Changed: 
  src/config.ts to map auth to the UI port without the nginx rewrite.


Check the version 
http://localhost:8082/data/xAPI/about

Use postman
-> Authorization 
  from the UI -> Settings -> Stores (create a new) -> Clients get user name = Key
  password = Secret
  (Basic Auth)

Header:
-> Needs X-Experience-API-Version: 1.0.3
Content-Type: application/json
Body: {
  "actor": {
  	"mbox": "mailto:marcin.wojtala@oup.com",
  	"name": "Marcin Wojtala"
  },
  "verb": {
  	"display": {
  		"en-GB": "accessed"
  	},
  	"id": "http://activitystrea.ms/schema/1.0/access"
  },
  "object": {
  	"id": "http://example.com/objectid",
  	"definition": {
  		"name": {
  			"en-GB":"Example Object"
  		}
  	}
  }
}

SHOULD Return an ARRAY in response.