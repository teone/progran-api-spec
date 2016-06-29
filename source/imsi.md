# Group IMSI 

Imsi is basic phone number object.
Before adding any imsi to profile (Refer to 2.5 ), it must be created.

## IMSI Collection [/onos/progran/imsi]

### List all IMSI [GET]

+ Response 200 (application/json)

        {
         "ImsiArray": [
              {
                "IMSI": "001020123456275",
                "UeStatus": 0,
                "Enodeb": "Enodeb-310",
                "DlMeasBitRate": 10000000,
                "UlMeasBitRate": 10000000
              },
              {
                  "IMSI": "001083903456275",
                  "UeStatus": 1,
                  "Enodeb": "Enodeb-320",
                  "DlMeasBitRate": 8000000,
                  "UlMeasBitRate": 8000000
                }
            ]
        }


### Create an IMSI [PUT]

+ Request (application/json)

        {
            "IMSI": "001020123456273"
        }

+ Response 200 (application/json)

        {    
          "Result": 1,
          "ErrCode": "Not Registered"
        }

## IMSI Details [/onos/progran/imsi/{imsi_number}]

### Get one IMSI [GET]

+ Parameters
    + imsi_number: "001020123456275" (string) - Number of the IMSI to retrieve

+ Response 200 (application/json)

        {
         "ImsiArray" : [{
          "IMSI": "001020123456275",
          "UeStatus": 0,
          "Enodeb": "Enodeb-310",
          "DlMeasBitRate": 10000000,
          "UlMeasBitRate": 10000000
          }]
        }

### Delete one IMSI [DELETE]

+ Parameters
    + imsi_number: "001020123456275" (string) - Number of the IMSI to delete

+ Response 204
 
## IMSI Profiles [/onos/progran/imsi/{imsi_number}/profile]

### Profile Name associated with Imsi [GET]

+ Parameters
    + imsi_number: "001020123456275" (string) - Number of the IMSI

+ Response 200 (application/json)

        [
          {
            "Name": "Profile-30",
            "DlSchedType": "RR",
            "DlAllocRBRate": 10,
            "UlSchedType": "RR",
            "UlAllocRBRate": 30,
            "Start": "15/05/2015 9:00",
            "End": "15/05/2015 18:00",
            "AdmControl": 0,
            "CellIndividualOffset": 0, 
            "Handover": {
              "A3offset": 2,
              "HysteresisA3": 1,
              "A5TriggerType": 0,
              "Rsrq": 1,
              "A5Thresh1Rsrp": -97,
              "A5Thresh1Rsrq": -10,
              "A5Thresh2Rsrp": -95,
              "A5Thresh2Rsrq": -8,
              "HysteresisA5": 1
            },
            "IMSIRuleArray" : [
              "001020123456273",
              "001020123456272" 
            ]
          },
          {
            "Name": "Profile-32",
            "DlSchedType": "RR",
            "DlAllocRBRate": 45,
            "UlSchedType": "RR",
            "UlAllocRBRate": 5,
            "Start": "15/05/2015 9:00",
            "End": "15/05/2015 18:00",
            "AdmControl": 0,
            "CellIndividualOffset": 0, 
            "Handover": {
              "A3offset": 2,
              "HysteresisA3": 1,
              "A5TriggerType": 0,
              "Rsrq": 1,
              "A5Thresh1Rsrp": -97,
              "A5Thresh1Rsrq": -10,
              "A5Thresh2Rsrp": -95,
              "A5Thresh2Rsrq": -8,
              "HysteresisA5": 1
            },
            "IMSIRuleArray" : [
              "001020123456273",
              "001020123456272" 
            ]
          }
        ]
        
## IMSI Profiles Details [/onos/progran/imsi/{imsi_number}/profile/{profile_name}]

### Delete one Profile from IMSI [DELETE]

+ Parameters
    + imsi_number: 001020123456275 (string) - Number of the IMSI to retrieve
    + profile_name: Profile30 (string) - Name of the Profiles

+ Response 204