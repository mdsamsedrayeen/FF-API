# Free Fire API Service Documentation

## Overview
This API service provides detailed information about players, maps, wishlists, and ban status in the game. Below are the endpoints and their respective functionalities.

## Base URL
```url
ff.samsedrain.com.np
```

## Endpoints

### 1. Player Info
**Endpoint:** `/info`  
**Description:** Fetches basic information about a player.  
**Parameters:**
- `uid` (integer, required): User ID
- `password` (string, required): User password
- `server` (string, required): Server code (e.g., "sg")

**Example Request:**
```
GET https://ff.samsedrain.com.np/info?uid=12345678&password={API_KEY}&server=sg
```

**Response:**
* 200 OK: Returns JSON data with the player's information:
```json
{
  "cached": true,
  "message": {
    "account": {
      "badge": "17",
      "bannerId": "901040014",
      "brPoint": "4370",
      "createdAt": "1512595169",
      "csPoint": "64",
      "exp": "1925563",
      "hasElitePass": true,
      "headPic": 902000154,
      "lastLogin": "1718213301",
      "level": "66",
      "likes": "3383012",
      "nickname": "FB:ㅤ@GMRemyX",
      "profile": {},
      "server": "SG",
      "uid": "12345678"
    },
    "guild": {
      "guildCapacity": "50",
      "guildLevel": "6",
      "id": "60893361",
      "leaderUID": "12345678",
      "name": "MᴜᴍᴍʏEᴠᴀTᴇᴀᴍ",
      "numberOfMembers": "43"
    },
    "guildLeader": {
      "badge": "17",
      "brPoint": "4370",
      "createdAt": "1512595169",
      "csPoint": "64",
      "exp": "1925563",
      "hasElitePass": true,
      "lastLogin": "1718213301",
      "level": "66",
      "likes": "3383012",
      "nickname": "FB:ㅤ@GMRemyX",
      "profile": {},
      "server": "SG",
      "uid": "12345678"
    },
    "socialStyle": {
      "bio": "FB & YT GM Remy | TikTok :gmremyx | IG GM Remy"
    }
  }
}
```

### 2. Full Player Info
**Endpoint:** `/playerinfo`  
**Description:** Fetches detailed information about a player.  
**Parameters:** 
- `uid` (string, required): User ID
- `password` (string, required): User password
- `server` (string, required): Server code (e.g., "sg")

**Example Request:**
```
GET https://ff.samsedrain.com.np/playerinfo?uid=12345678&password={API_KEY}&server=sg
```

**Response:**
* 200 OK: Returns JSON data with the player's information:
```json
{
  "cached": false,
  "message": {
    "basicInfo": {
      "accountId": "12345678",
      "accountPrefers": {},
      "accountType": 1,
      "badgeCnt": 17,
      "badgeId": 1001000073,
      "bannerId": 901040014,
      "createAt": "1512595169",
      "csMaxRank": 216,
      "csRank": 216,
      "csRankingPoints": 64,
      "exp": 1925563,
      "externalIconInfo": {
        "showType": "ExternalIconShowType_FRIEND",
        "status": "ExternalIconStatus_NOT_IN_USE"
      },
      "hasElitePass": true,
      "headPic": 902000154,
      "lastLoginAt": "1718213301",
      "level": 66,
      "liked": 3383012,
      "maxRank": 221,
      "nickname": "FB:ㅤ@GMRemyX",
      "rank": 221,
      "rankingPoints": 4370,
      "region": "SG",
      "releaseVersion": "OB44",
      "role": 4,
      "seasonId": 39,
      "showBrRank": true,
      "showCsRank": true,
      "socialHighLightsWithBasicInfo": {},
      "title": 904090023,
      "weaponSkinShows": [907103421, 912042002, 914000002]
    },
    "captainBasicInfo": {
      "accountId": "12345678",
      "accountPrefers": {},
      "accountType": 1,
      "badgeCnt": 17,
      "badgeId": 1001000073,
      "bannerId": 901040014,
      "createAt": "1512595169",
      "csMaxRank": 216,
      "csRank": 216,
      "csRankingPoints": 64,
      "exp": 1925563,
      "externalIconInfo": {
        "showType": "ExternalIconShowType_FRIEND",
        "status": "ExternalIconStatus_NOT_IN_USE"
      },
      "hasElitePass": true,
      "headPic": 902000154,
      "lastLoginAt": "1718213301",
      "level": 66,
      "liked": 3383012,
      "maxRank": 221,
      "nickname": "FB:ㅤ@GMRemyX",
      "rank": 221,
      "rankingPoints": 4370,
      "region": "SG",
      "releaseVersion": "OB44",
      "role": 4,
      "seasonId": 39,
      "showBrRank": true,
      "showCsRank": true,
      "socialHighLightsWithBasicInfo": {},
      "title": 904090023,
      "weaponSkinShows": [907103421, 912042002, 914000002]
    },
    "clanBasicInfo": {
      "capacity": 50,
      "captainId": "12345678",
      "clanId": "60893361",
      "clanLevel": 6,
      "clanName": "MᴜᴍᴍʏEᴠᴀTᴇᴀᴍ",
      "memberNum": 43
    },
    "creditScoreInfo": {
      "creditScore": 100,
      "periodicSummaryEndTime": "1717984821",
      "rewardState": "REWARD_STATE_UNCLAIMED"
    },
    "diamondCostRes": {
      "diamondCost": 390
    },
    "equippedAch": [
      {
        "achId": 32006,
        "level": 2
      },
      {
        "achId": 21009,
        "level": 3
      },
      {
        "achId": 21006,
        "level": 3
      },
      {
        "achId": 21008,
        "level": 3
      }
    ],
    "historyEpInfo": [
      {
        "badgeCnt": 121,
        "bpIcon": "UI_BP_Emoji_Videogame",
        "epBadge": 1001000072,
        "epEventId": 72,
        "eventName": "T_44_H_BP72_NAME",
        "maxLevel": 100,
        "ownedPass": true
      },
      {
        "badgeCnt": 100,
        "bpIcon": "UI_BP_Emoji_Pointed",
        "epBadge": 1001000071,
        "epEventId": 71,
        "eventName": "T_43_H_BP71_NAME",
        "maxLevel": 100,
        "ownedPass": true
      },
      {
        "badgeCnt": 107,
        "bpIcon": "UI_BP_Emoji_Frog",
        "epBadge": 1001000070,
        "epEventId": 70,
        "eventName": "T_43_H_BP70_NAME",
        "maxLevel": 100,
        "ownedPass": true
      },
      {
        "badgeCnt": 101,
        "bpIcon": "UI_BP_Emoji_Asura",
        "epBadge": 1001000069,
        "epEventId": 69,
        "eventName": "T_43_H_BP69_NAME",
        "maxLevel": 100,
        "ownedPass": true
      },
      {
        "badgeCnt": 163,
        "bpIcon": "UI_BP_Emoji_Electri",
        "epBadge": 1001000068,
        "epEventId": 68,
        "eventName": "T_42_H_BP68_NAME",
        "maxLevel": 150,
        "ownedPass": true
      },
      {
        "badgeCnt": 155,
        "bpIcon": "UI_BP_Emoji_Watcher",
        "epBadge": 1001000067,
        "epEventId": 67,
        "eventName": "T_42_H_BP67_NAME",
        "maxLevel": 150,
        "ownedPass": true
      },
      {
        "badgeCnt": 178,
        "bpIcon": "UI_BP_Emoji_Puppets",
        "epBadge": 1001000066,
        "epEventId": 66,
        "eventName": "T_41_H_BP66_NAME",
        "maxLevel": 150,
        "ownedPass": true
      },
      {
        "badgeCnt": 134,
        "bpIcon": "UI_BP_Emoji_Poseidon",
        "epBadge": 1001000065,
        "epEventId": 65,
        "eventName": "T_41_H_BP65_NAME",
        "maxLevel": 150,
        "ownedPass": true
      },
      {
        "badgeCnt": 97,
        "bpIcon": "UI_BP_Emoji_Cook",
        "epBadge": 1001000064,
        "epEventId": 64,
        "eventName": "T_40_H_BP64_NAME",
        "maxLevel": 100,
        "ownedPass": true
      },
      {
        "badgeCnt": 95,
        "bpIcon": "UI_BP_Emoji_Bored",
        "epBadge": 1001000063,
        "epEventId": 63,
        "eventName": "T_40_H_BP63_NAME",
        "maxLevel": 100,
        "ownedPass": true
      }
    ],
    "intfUserMatchInfo": {
      "clanId": "60893361",
      "clanName": "MᴜᴍᴍʏEᴠᴀTᴇᴀᴍ",
      "leaderId": "12345678"
    },
    "playerCustomSets": [],
    "rankInfo": {
      "brRank": 221,
      "brRankingPoints": 4370,
      "csRank": 216,
      "csRankingPoints": 64
    },
    "roleInClans": {
      "captainInClan": true
    },
    "socialHighLights": {
      "highlightList": []
    },
    "socialInfo": {
      "bio": "FB & YT GM Remy | TikTok :gmremyx | IG GM Remy",
      "followerNum": 148,
      "followingNum": 0
    },
    "userBriefInfo": {
      "badgeCnt": 17,
      "brPoint": 4370,
      "createAt": "1512595169",
      "csPoint": 64,
      "exp": 1925563,
      "lastLoginAt": "1718213301",
      "level": 66,
      "liked": 3383012,
      "nickname": "FB:ㅤ@GMRemyX",
      "uid": "12345678"
    }
  }
}
```

### 3. Map Info
**Endpoint:** `/mapinfo`  
**Description:** Fetches information about a specific map.  
**Parameters:**
- `map` (string, required): Map code
- `password` (string, required): User password
- `server` (string, required): Server code (e.g., "sg")

**Example Request:**
```
GET https://ff.samsedrain.com.np/mapinfo?map=FFMAPCODE&password={API_KEY}&server=sg
```

**Response:**
* 200 OK: Returns JSON data with the player's information:
```json
{
  "message": {
    "mapInfo": {
      "createdAt": "1698415464",
      "desc": "Horror map of Halloween",
      "dislikes": "10",
      "likes": "34",
      "name": "X--RI-DR",
      "ownerName": "NOc1cb8df09b",
      "ownerUid": "7385902489",
      "subs": "70",
      "updatedAt": "1714051231"
    }
  }
}
```

### 4. Wishlist Info
**Endpoint:** `/wishlist`  
**Description:** Fetches the wishlist items of a player.  
**Parameters:**
- `uid` (string, required): User ID
- `password` (string, required): User password
- `server` (string, required): Server code (e.g., "sg")

**Example Request:**
```
GET https://ff.samsedrain.com.np/wishlist?uid=12345678&password={API_KEY}&server=sg
```

**Response:**
* 200 OK: Returns JSON data with the player's information:
```json
{
  "message": {
    "items": [
      {
        "addedAt": "1716197514",
        "itemId": "911004401"
      }
    ]
  }
}
```

### 5. Ban Check
**Endpoint:** `/isbanned`  
**Description:** Checks if a player is banned.  
**Parameters:**
- `uid` (string, required): User ID
- `password` (string, required): User password
- `server` (string, required): Server code (e.g., "sg")

**Example Request:**
```
GET https://ff.samsedrain.com.np/isbanned?uid=12345678&password={API_KEY}&server=sg
```

**Response:**
* 200 OK: Returns JSON data with the player's information:
```json
{
  "message": 0
}
```
**Note:** The response will be `0` if the user is not banned and `1` if the user is banned.

### 6. Profile Board

**Endpoint:** `/profile`  
**Description:** Generates a profile board image for a player.  
**Parameters:**
- `password` (string, required): Your API key.
- `banner` (integer, required): Banner ID to be used on the profile board.
- `avatar` (integer, required): Avatar ID to be used on the profile board.
- `name` (string, required): Player's name to be displayed on the profile board.
- `level` (integer, required): Player's level.
- `uid` (string, required): User ID.

**Example Request:**
```
GET https://ff.samsedrain.com.np/profile?password=YOUR_KEY&banner=901040014&avatar=902000154&name=%EF%BC%B3%EF%BC%B8%EF%BC%B3_%EF%BC%AB%EF%BC%A9%EF%BC%A2%EF%BC%AF%EA%94%AA&level=10&uid=12345678
```

**Response:**
This endpoint returns a `.webp` image that contains the player's profile board with the specified banner, avatar, name, level, and user ID.

**Usage Example:**
To retrieve and display the profile board image, you can use the following curl command:

```sh
curl -O "https://ff.samsedrain.com.np/profile?password=YOUR_KEY&banner=901040014&avatar=902000154&name=Example_Name&level=10&uid=12345678"
```

Make sure to replace `YOUR_KEY` with your actual API key. The command will save the profile board image in the current directory.

## Authentication
Each endpoint requires authentication using the `password` parameters. Make sure to pass these parameters correctly in your requests.

## Errors
All endpoints will return appropriate HTTP status codes to indicate success or failure. Common HTTP status codes include:
- `200 OK`: Request was successful.
- `400 Bad Request`: There was an error with the request parameters.
- `401 Unauthorized`: Authentication failed.
- `404 Not Found`: The requested resource was not found.
- `500 Internal Server Error`: An error occurred on the server.
- Note: Temporary We use error key in response json for error and message key as a custom error message all status code is 200 but soon it will be changed 

## Caching
The `cached` field in the response indicates whether the data was retrieved from the cache. This can help in determining if the data is the latest or from a previous request.

## Usage Example
Below is an example of how to make a request to the `playerinfo` endpoint using curl:

```sh
curl -X GET "https://ff.samsedrain.com.np/playerinfo?uid=12345678&password={API_KEY}&server=sg"
```

## Conclusion
This API service provides comprehensive data on players, maps, and other game-related information. Ensure that all parameters are correctly provided to avoid errors. For further assistance, refer to the detailed responses and status codes.
