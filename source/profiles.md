# Group Profiles

## Profiles Collection [/api/profile]

### List all Profiles [GET]

+ Response 200 (application/json)
      
        [
          {
            "Name": "Profile-30"
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
              "HysteresisA5": 1,
            }
            "IMSIRuleArray" : [
              "001020123456273",
              "001020123456272" 
            ]
          },
          {
            "Name": "Profile-31"
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
              "HysteresisA5": 1,
            }
            "IMSIRuleArray" : [
              "001020123456273",
              "001020123456272" 
            ]
          },
          {
            "Name": "Profile-32"
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
              "HysteresisA5": 1,
            }
            "IMSIRuleArray" : [
              "001020123456273",
              "001020123456272" 
            ]
          }
        ]

### Create an Profiles [PUT]

+ Request (application/json)

        {
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
            "HysteresisA5"  : 1,
          }
        }



+ Response 200 (application/json)

        {    
          "Result": 1,
          "ErrCode": "Not Registered"
        }

## Profiles Details [/api/profile/:profile_name]

### Get one Profiles [GET]

+ Parameters
    + profile_name: "Profile-30" (string) - Name of the Profiles to retrieve

+ Response 200 (application/json)

        {
            "Name": "Profile-30"
            "DlSchedType": "RR",
            "DlAllocRBRate": 30,
            "UlSchedType": "RR",
            "UlAllocRBRate": 30,
            "Start": "15/05/2015 9:00",
            "End": "15/05/2015 18:00",
            "AdmControl": 0
            "CellIndividualOffset": 0, 
            "Handover"    : {
              "A3offset"      : 2,
              "HysteresisA3"  : 1,
              "A5TriggerType" : 0,
              "Rsrq" : 1,
              "A5Thresh1Rsrp" : -97,
              "A5Thresh1Rsrq" : -10,
              "A5Thresh2Rsrp" : -95,
              "A5Thresh2Rsrq" : -8,
              "HysteresisA5"  : 1,
            }
            "IMSIRuleArray" : [
              "001020123456273",
              "001020123456272" 
            ]
          }

### Delete one Profiles [DELETE]

+ Parameters
    + profile_name: "Profile-30" (string) - Name of the Profiles to delete

+ Response 204

## Profiles IMSI's Collection [/api/profile/:profile_name/imsi]

### Add an IMSI to a Profile [PUT]

+ Parameters
    + profile_name: "Profile-30" (string) - Name of the Profiles to retrieve

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
    + profile_name: "Profile-30" (string) - Name of the Profiles to retrieve

+ Response 204

## Profiles IMSI's Details [/api/profile/:profile_name/:imsi_number]

### Delete one IMSI from a Profile [DELETE]

+ Parameters
    + profile_name: "Profile-30" (string) - Name of the Profiles to retrieve
    + imsi_number: "001020123456275" (string) - Number of the IMSI

+ Response 204
