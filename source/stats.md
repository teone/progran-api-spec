# Group Stats

# IMSI stats [/api/stats/imsi/{imsi}/{counts}]

### Get Stats [GET]

+ Parameters
    + imsi: "001020123456275" (string) - Number of the IMSI to retrieve
    + counts: "10" (string) - Value can be 10, 20 or  "mean"

+ Response 200 (application/json)
      
        [
          {
            "Time"      :   123333   //Log time in milliseconds 
            "DlBitrate" :   10,     //Download bitrate  
            "UlBitrate" :   20      // Upload bitrate 
          },
          {
            "Time"      :   127333   //Log time in milliseconds
            "DlBitrate" :   8,     //Download bitrate  
            "UlBitrate" :   0      // Upload bitrate 
          },
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
                "Time"      :   123333   //Log time in miliseconds
                "DlBitrate" :   10,     //Download bitrate  
                "UlBitrate" :   20      // Upload bitrate 
              },
              {
                "Time"      :   126333   //Log time in miliseconds
                "DlBitrate" :   8,     //Download bitrate  
                "UlBitrate" :   0      // Upload bitrate 
              },
            ]
          },
          {
            "Enodeb"  : 315,
            "StatsArray" :[
                {
                  "Time"      :   127333   //Log time in miliseconds
                  "DlBitrate" :   10,     //Download bitrate  
                  "UlBitrate" :   20      // Upload bitrate 
                },
                {
                  "Time"      :   129333   //Log time in miliseconds
                  "DlBitrate" :   8,     //Download bitrate  
                  "UlBitrate" :   0      // Upload bitrate 
                },
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
                "Time"      :   123333   //Log time in miliseconds
                "DlBitrate" :   10,     //Download bitrate  
                "UlBitrate" :   20      // Upload bitrate 
              },
              {
                "Time"      :   129333   //Log time in miliseconds
                "DlBitrate" :   8,     //Download bitrate  
                "UlBitrate" :   0      // Upload bitrate 
              }
            ]
          },
          {
            "Profile"  : "Profile-1"
            "StatsArray" :[
              {
                "Time"      :   121333   //Log time in miliseconds
                "DlBitrate" :   10,     //Download bitrate  
                "UlBitrate" :   20      // Upload bitrate 
              },
              {
                "Time"      :   127333   //Log time in miliseconds
                "DlBitrate" :   8,     //Download bitrate  
                "UlBitrate" :   0      // Upload bitrate 
              }
            ]
          }
        ]

