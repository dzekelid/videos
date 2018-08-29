{
  "info": {
    "name": "Entertainment Express Returns a URL to a requested video.",
    "_postman_id": "e59e1b38-9d71-471a-8805-580a8d3dc3f5",
    "description": "Returns a URL to the requested video. [Video Format Specs](https://developer.iva-api.com/docs/v1/video-formats)\n\n**Formats:** MP4 = 4, HLS = 11, Dash = 14, HSS = 12, HDS = 13\n\n**MP4 KbRate:** 80, 212, 450, 750, 1500, 2500(HD sources only), 5000 (sources >=  1080p)  \n\n**Adaptive Min/Max rate:** 212000, 350000, 600000, 1200000, 2000000, 2500000, 3500000  \n\n `URLs requested with a Demo account will always return max 750 kbps video.  Full commercial account required for higher bitrates.`",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Videos",
      "item": [
        {
          "id": "bdf93aa0-aefe-45b0-aa5e-40b451f7de52",
          "name": "GetVideo",
          "request": {
            "url": {
              "protocol": "http",
              "host": "ee.iva-api.com",
              "path": [
                "Videos/GetVideo/:Id"
              ],
              "query": [
                {
                  "key": "end",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "Expires",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "Format",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "KbRate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "MaxRate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "MinRate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "ReportTag",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "Id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a URL to the requested video. [Video Format Specs](https://developer.iva-api.com/docs/v1/video-formats)\n\n**Formats:** MP4 = 4, HLS = 11, Dash = 14, HSS = 12, HDS = 13\n\n**MP4 KbRate:** 80, 212, 450, 750, 1500, 2500(HD sources only), 5000 (sources >=  1080p)  \n\n**Adaptive Min/Max rate:** 212000, 350000, 600000, 1200000, 2000000, 2500000, 3500000  \n\n `URLs requested with a Demo account will always return max 750 kbps video.  Full commercial account required for higher bitrates.`"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5991c430-0365-472e-8c09-3e3225b94262"
            }
          ]
        }
      ]
    }
  ]
}