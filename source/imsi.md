# Group IMSI 

Imsi is basic phone number object.
Before adding any imsi to profile (Refer to 2.5 ), it must be created.

## IMSI Collection [/api/imsi]

### List all IMSI [GET]

+ Response 200 (application/json)

        [
          {
            "IMSI": "001020123456275",
            "UeStatus": 0
            "Enodeb": “Enodeb-310”
            "DlMeasBitRate": 10000000,
            "UlMeasBitRate": 10000000,
          }
        ]


### Create an IMSI [PUT]

+ Request (application/json)

        {
            "IMSI": "001020123456273",
        }

+ Response 200 (application/json)

        {    
          "Result": 1,
          "ErrCode": "Not Registered"
        }

## IMSI Details [/api/imsi/{imsi_number}]

### Get one IMSI [GET]

+ Parameters
    + imsi_number: "001020123456275" (string) - Number of the IMSI to retrieve

+ Response 200 (application/json)

        {
          "IMSI": "001020123456275",
          "UeStatus": 0
          "Enodeb": “Enodeb-310”
          "DlMeasBitRate": 10000000,
          "UlMeasBitRate": 10000000,
        }

### Delete one IMSI [DELETE]

+ Parameters
    + imsi_number: "001020123456275" (string) - Number of the IMSI to delete

+ Response 204
 
## IMSI Profiles [/api/imsi/{imsi_number}/profile]

### Profile Name associated with Imsi [GET]

+ Parameters
    + imsi_number: "001020123456275" (string) - Number of the IMSI

+ Response 200 (application/json)

        [      
          "Profile1",
          "Profile2",
          "Profile3"
        ]