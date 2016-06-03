# Group E NODE B

## E NODE B Collection [/api/enodeb]

### List all E NODE B [GET]

+ Response 200 (application/json)
      
        [
          {
            "eNBId": 591,
            "Description": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec euismod ornare eros, sit amet euismod mauris. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed sit amet pharetra sapien, non interdum ante.",
            "Status": 1,
            "IpAddr": "10.1.49.200",
            "GpsCoordinate": {
              "Latitude": 37.7749290,
              "Longitude": -122.4194160 
            },
            "ProfileArray" :[
              " Profile1",
              " Profile2",
              " Profile3"
            ]
          },
          {
            "eNBId": 592,
            "Description": "Proin et sapien sit amet ligula elementum molestie et eu ligula. Integer non urna vitae velit consectetur volutpat eget hendrerit eros. Nam varius, ex sit amet feugiat condimentum, velit risus iaculis elit, eu hendrerit est tortor eget augue.",
            "Status": 1,
            "IpAddr": "10.1.49.200",
            "GpsCoordinate": {
              "Latitude": 37.4418830,
              "Longitude": -122.1430190 
            },
            "ProfileArray" :[
              " Profile1",
              " Profile2",
              " Profile3"
            ]
          },
          {
            "eNBId": 593,
            "Description": "Nunc quam tortor, ullamcorper at bibendum eget, vehicula eget neque. Maecenas nulla ligula, sodales at venenatis at, vehicula vel nunc. Mauris et tincidunt nisl.",
            "Status": 1,
            "IpAddr": "10.1.49.200",
            "GpsCoordinate": {
              "Latitude": 37.8043640,
              "Longitude": -122.2711140 
            },
            "ProfileArray" :[
              " Profile1",
              " Profile2",
              " Profile3"
            ]
          }

        ]

### Create an E NODE B [PUT]

+ Request (application/json)

        {
          "eNBId": 591,
          "Description": "Maslak-12",
          "IpAddr": "10.1.49.200"
        }


+ Response 200 (application/json)

        {    
          "Result": 1,
          "ErrCode": "Not Registered"
        }

## E NODE B Details [/api/enodeb/:eNBId]

### Get one E NODE B [GET]

+ Parameters
    + eNBId: 591 (number) - Number of the E NODE B to retrieve

+ Response 200 (application/json)

        {
          "eNBId": 591,
          "Description": "Maslak-12",
          "Status": 1,
          "IpAddr": "10.1.49.200",
          "GpsCoordinate": {
            "Latitude": 37.492425,
            "Longitude": 127.031008
          }
          "ProfileArray" :[
            " Profile1",
            " Profile2",
            " Profile3"
          ]
        }

### Delete one E NODE B [DELETE]

+ Parameters
    + eNBId: 591 (number) - Number of the E NODE B to delete

+ Response 204

## E NODE B Profiles Collection [/api/enodeb/:eNBId/profile]

### Get a Profile list associated to E NODE B [GET]

+ Parameters
    + eNBId: 591 (number) - Number of the E NODE B to retrieve

+ Response 200 (application/json)
      
        [
          {
            "Name": "Profile-30",
            "DlSchedType": "RR",
            "DlAllocRBRate": 30,
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
            "Name": "Profile-31",
            "DlSchedType": "RR",
            "DlAllocRBRate": 30,
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
            "DlAllocRBRate": 30,
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
          }
        ]

### Add an Profile to E NODE B [PUT]

+ Parameters
    + eNBId: 591 (number) - Number of the E NODE B to retrieve

+ Request (application/json)

        {
          "ProfileArray" :[
            "Profile1",
            "Profile2"
          ]
        }
+ Response 200 (application/json)

        {    
          "Result": 1,
          "ErrCode": "Not Registered"
        }

### Delete all Profile from E NODE B [DELETE]

+ Parameters
    + eNBId: 591 (number) - Number of the E NODE B to retrieve

+ Response 204

## E NODE B Profiles Details [/api/profile/:eNBId/:profile_name]

### Delete one Profile from E NODE B [DELETE]

+ Parameters
    + eNBId: 591 (number) - Number of the E NODE B to retrieve
    + profile_name: "Profile-30" (string) - Name of the Profiles

+ Response 204

