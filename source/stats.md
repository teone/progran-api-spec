# Group Stats

# IMSI stats [/onos/progran/stats/imsi/{imsi}/{counts}]

### Get Stats [GET]

+ Parameters
    + imsi: "001020123456275" (string) - Number of the IMSI to retrieve
    + counts: "10" (string) - Value can be 10, 20 or  "mean"

+ Response 200 (application/json)
      
        [
          {
            "Time"      :   123333 
            "DlBitrate" :   10,
            "UlBitrate" :   20
          },
          {
            "Time"      :   127333
            "DlBitrate" :   8,
            "UlBitrate" :   0
          }
        ]

## Profile stats [/onos/progran/stats/profile/{profile_name}/{counts}]

### Get Stats [GET]

+ Parameters
    + profile_name: "Profile-30" (string) - Name of the Profiles to retrieve
    + counts: "10" (string) - Value can be 10, 20 or  "mean"

+ Response 200 (application/json)
      
        [
          {
            "Enodeb"  : 312,
            "StatsArray" :[
              { 
                "Time"      :   123333
                "DlBitrate" :   10,
                "UlBitrate" :   20 
              },
              {
                "Time"      :   126333
                "DlBitrate" :   8,
                "UlBitrate" :   0 
              }
            ]
          },
          {
            "Enodeb"  : 315,
            "StatsArray" :[
                {
                  "Time"      :   127333
                  "DlBitrate" :   10,
                  "UlBitrate" :   20 
                },
                {
                  "Time"      :   129333
                  "DlBitrate" :   8,
                  "UlBitrate" :   0 
                }
              }
            ]
          }
        ]

## E NODE B stats [/onos/progran/stats/enodeb/{eNBId}/{counts}]

### Get Stats [GET]

+ Parameters
    + eNBId: "591" (string) - Name of the Profiles to retrieve
    + counts: "10" (string) - Value can be 10, 20 or  "mean"

+ Response 200 (application/json)

        {
          "ConnectedUE": 246,
          "ActiveProfiles": 827,
          "TotalProfiles": 827,
          "Uptime": 293894,
          "ProfileArray": [
            {
              "Profile"  : "Profile-1",
              "StatsArray" :[
                {
                  "Time"      :   1464990095,
                  "DlBitrate" :   10,
                  "UlBitrate" :   20 
                },
                {
                  "Time"      :   1464986495,
                  "DlBitrate" :   10,
                  "UlBitrate" :   30 
                },
                {
                  "Time"      :   1464982895,
                  "DlBitrate" :   8,
                  "UlBitrate" :   10 
                }
              ]
            },
            {
              "Profile"  : "Profile-2",
              "StatsArray" :[
                {
                  "Time"      :   1464990095,
                  "DlBitrate" :   13,
                  "UlBitrate" :   25 
                },
                {
                  "Time"      :   1464986495,
                  "DlBitrate" :   10,
                  "UlBitrate" :   12 
                },
                {
                  "Time"      :   1464982895,
                  "DlBitrate" :   4,
                  "UlBitrate" :   26 
                }
              ]
            }
          ]
        }

