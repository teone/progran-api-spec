# Group E NODE B

## E NODE B Collection [/api/enodeb]

### List all E NODE B [GET]

+ Response 200 (application/json)
      
        [
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
    + eNBId: "591" (number) - Number of the E NODE B to retrieve

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
    + eNBId: "591" (number) - Number of the E NODE B to delete

+ Response 204

## E NODE B Profiles Collection [/api/enodeb/:eNBId/profile]

### Add an Profile to E NODE B [PUT]

+ Parameters
    + eNBId: "591" (number) - Number of the E NODE B to retrieve

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
    + eNBId: "591" (number) - Number of the E NODE B to retrieve

+ Response 204

## E NODE B Profiles Details [/api/profile/:eNBId/:profile_name]

### Delete one Profile from E NODE B [DELETE]

+ Parameters
    + eNBId: "591" (number) - Number of the E NODE B to retrieve
    + profile_name: "Profile-30" (string) - Name of the Profiles

+ Response 204

