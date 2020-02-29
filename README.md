# COVID-19-API [![Docker Pulls](https://img.shields.io/docker/pulls/laeyoung/wuhan-coronavirus-api?style=plastic)](https://hub.docker.com/r/laeyoung/wuhan-coronavirus-api/)


API Service for tracking the COVID-19

## Try it
[![Run on Ainize](https://ainize.ai/static/images/run_on_ainize_button.svg)](https://ainize.web.app/redirect?git_repo=github.com/Laeyoung/Wuhan-Coronavirus-API)

## API Document

### Endpoint
https://wuhan-coronavirus-api.laeyoung.endpoint.ainize.ai/

### Brief

**Request:**
```json
GET /jhu-edu/brief
```
**Successful Response:**
```json
HTTP/1.1 200 OK
Content-Type: application/json

{
	"confirmed": 7783,
	"deaths": 170,
	"recovered": 133
}
```

**Curl:**
```sh
curl -X GET "https://wuhan-coronavirus-api.laeyoung.endpoint.ainize.ai/jhu-edu/brief" -H "accept: application/json"
```

**Browser:**
https://wuhan-coronavirus-api.laeyoung.endpoint.ainize.ai/jhu-edu/brief

### Latest

**Request:**
```json
GET /jhu-edu/latest
```
**Successful Response:**
```json
HTTP/1.1 200 OK
Content-Type: application/json

[
  {
    "provincestate": "Anhui",
    "countryregion": "Mainland China",
    "lastupdate": "2020-02-29T07:21:21.001Z",
    "confirmed": 990,
    "deaths": 6,
    "recovered": 821,
    "location": {
      "lat": 31.8257,
      "lng": 117.2264
    }
  }, {
    "provincestate": "Beijing",
    "countryregion": "Mainland China",
    "lastupdate": "2020-02-29T07:21:21.001Z",
    "confirmed": 410,
    "deaths": 7,
    "recovered": 257,
    "location": {
      "lat": 40.1824,
      "lng": 116.4142
    }
  }, ...
]
```

**Curl:**
```sh
curl -X GET "https://wuhan-coronavirus-api.laeyoung.endpoint.ainize.ai/jhu-edu/latest" -H "accept: application/json"
```

**Browser:**
https://wuhan-coronavirus-api.laeyoung.endpoint.ainize.ai/jhu-edu/latest

### Services using Wuhan-Coronavirus-API
- https://corona-three.now.sh/

### Original data source
[Novel Coronavirus (COVID-19) Cases](https://github.com/CSSEGISandData/COVID-19), provided by JHU CSSE
