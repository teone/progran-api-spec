# Group Profiles

## Profiles Collection [/onos/progran/profile]

### List all Profiles [GET]

+ Response 200 (application/json)
      
        {
            "ProfileArray" : [
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
        }

### Create an Profiles [PUT]

+ Request (application/json)

        {
            "ProfileArray" : {
              "Name" : "Profile-30",
              "DlSchedType"   : "RR",
              "DlAllocRBRate" : 30,
              "UlSchedType"   : "RR",
              "UlAllocRBRate" : 30,
              "Start": "15/05/2015 9:00",
              "End" :"15/05/2015 18:00",
              "AdmControl : 0,
              "CellIndividualOffset:0, 
              "Handover": {
                "A3offset"      : 2,
                "HysteresisA3"  : 1,
                "A5TriggerType" : 0,
                "Rsrq" : 1,
                "A5Thresh1Rsrp" : -97,
                "A5Thresh1Rsrq" : -10,
                "A5Thresh2Rsrp" : -95,
                "A5Thresh2Rsrq" : -8,
                "HysteresisA5"  : 1
              }
          }
        }



+ Response 200 (application/json)

        {    
          "Result": 1,
          "ErrCode": "Not Registered"
        }

## Profiles Details [/onos/progran/profile/{profile_name}]

### Get one Profiles [GET]

+ Parameters
    + profile_name: Profile30 (string) - Name of the Profiles to retrieve

+ Response 200 (application/json)

        {
            "ProfileArray": {
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
            }
        }

### Delete one Profiles [DELETE]

+ Parameters
    + profile_name: Profile30 (string) - Name of the Profiles to delete

+ Response 204

## Profiles IMSI's Collection [/onos/progran/profile/{profile_name}/imsi]

## Get IMSI list for a profile [GET]

+ Parameters
    + profile_name: Profile30 (string) - Name of the Profiles to retrieve

+ Response 200 (application/json)
    
         [
           {
             "IMSI": "001020123456275",
             "UeStatus": 0,
             "Enodeb": "Enodeb-310",
             "DlMeasBitRate": 10000000,
             "UlMeasBitRate": 10000000
           }
         ]

### Add an IMSI to a Profile [PUT]

+ Parameters
    + profile_name: Profile30 (string) - Name of the Profiles to retrieve

+ Request (application/json)

        {
          "IMSIRuleArray" : [
            "001020123456273",
            "001020123456272"
          ]
        }
+ Response 200 (application/json)

        {    
          "Result": 1,
          "ErrCode": "Not Registered"
        }

### Delete all IMSI from a Profile [DELETE]

+ Parameters
    + profile_name: Profile30 (string) - Name of the Profiles to retrieve

+ Response 204

## Profiles IMSI's Details [/onos/progran/profile/{profile_name}/imsi/{imsi_number}]

### Delete one IMSI from a Profile [DELETE]

+ Parameters
    + profile_name: Profile30 (string) - Name of the Profiles to retrieve
    + imsi_number: "001020123456275" (string) - Number of the IMSI

+ Response 204

## Profiles E Node B's Collection [/onos/progran/profile/{profile_name}/enodeb]

## Get E Node B list for a profile [GET]

+ Parameters
    + profile_name: Profile30 (string) - Name of the Profiles to retrieve

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
                 
### Delete all E Node B from a Profile [DELETE]

+ Parameters
    + profile_name: Profile30 (string) - Name of the Profiles to retrieve

+ Response 204

## Profiles E Node B's Details [/onos/progran/profile/{profile_name}/enodeb/{enode_id}]

### Delete one E Node B from a Profile [DELETE]

+ Parameters
    + profile_name: Profile30 (string) - Name of the Profiles to retrieve
    + enode_id: 593 (number) - Number of the IMSI

+ Response 204