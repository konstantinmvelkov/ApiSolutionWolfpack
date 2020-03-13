# ApiSolutionWolfpack
The solution includes 3 entities - Packs, Wolves and their relation WolfPacks.

They are managed and stored in three inmemory databases. Such are used instead of sqlserver for demonstrative purposes.
It is assumed that wolves are identified by ids and that packs are identified by names.
Packs consist of one or more wolves. They are created through a post request to WolfPacks.
Therefore making this post request creates a pack in Packs if one is not present.

Location of a Wolf is represent by a PointF structure - the x coordinate representing latitude and the y representing longitude.

All tests of the Restful Apis are conducted with Postman. There is no SSL certificate verification, so when calling the api's this option should be turned off.

## Wolves

POST: api/Wolves

sample:

        {	    
            "wolfid":1307436,
            "name": "Konstantin",
            "gender": 1,
            "birthdate":"1999-03-24",
            "location": {"x":51.449409,"y":5.494774}
        }

GET: api/Wolves


  
GET: api/Wolves/id

PUT: api/Wolves/id

DELETE: api/Wolves/id

GET: api/Wolves/id/location

PATCH: api/Wolves/id/location

sample:

        {
          "x":1.2,
          "y":3.4567
        }
## WolfPacks

POST: api/WolfPacks

sample -

        {
          "wolfid":1307436,
          "packname":"Alpha"
        }

GET: api/WolfPacks

GET: api/WolfPacks/packname

GET: api/WolfPacks/packname/id

DELETE: api/WolfPacks/packname

DELETE: api/WolfPacks/packname/id

## Packs

GET: api/Packs

GET: api/Packs/packname

DELETE: api/Packs/packname
