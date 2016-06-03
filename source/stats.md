# Group Stats

# IMSI stats [/api/stats/imsi/{imsi}/{counts}]

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

## Profile stats [/api/stats/profile/{profile_name}/{counts}]

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

## E NODE B stats [/api/stats/enodeb/{eNBId}/{counts}]

### Get Stats [GET]

+ Parameters
    + eNBId: "591" (string) - Name of the Profiles to retrieve
    + counts: "10" (string) - Value can be 10, 20 or  "mean"

+ Response 200 (application/json)

        [
          {
            "Profile"  : "Profile-1",
            "StatsArray" :[
              {
                "Time"      :   123333
                "DlBitrate" :   10,
                "UlBitrate" :   20 
              },
              {
                "Time"      :   129333
                "DlBitrate" :   8,
                "UlBitrate" :   0 
              }
            ]
          },
          {
            "Profile"  : "Profile-1"
            "StatsArray" :[
              {
                "Time"      :   121333
                "DlBitrate" :   10,
                "UlBitrate" :   20 
              },
              {
                "Time"      :   127333
                "DlBitrate" :   8,
                "UlBitrate" :   0 
              }
            ]
          }
        ]

