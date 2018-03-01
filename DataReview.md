# Data Review

  - Refugee crisis visualization
  - 3, maybe 4 chapters
  - provide a global overview/deep dive on the refugee crisis.


## Chapter 1 - Chaos

### Data Sources
  1. [ACLED - Armed Conflict Location & Event Data](https://www.acleddata.com/data/)
    - *Size*: ~150Mb
    - *Total data points*: 258,003 (__207,234__ after truncated)
    - *Timeframe*: __2010__ to __2018__
    - *Scale*: Africa, Mid-East, Asia
    - *Keywords*: Political violence, War, Conflict, crisis mapping
    - *sample data(exclude irrelevant filed)*:
      ```JS
      {
        //timestamp
        event_date: '31 December 2014',
        //conflict type
        event_type: 'Violence against civilians',
        //involved party
        actor1: 'Seleka Militia',
        assoc_actor_1: 'Fulani Ethnic Militia (Central African Republic)',
        inter1: '3',
        actor2: 'Civilians (Central African Republic)',
        assoc_actor_2: '',
        inter2: '7',
        interaction: '37',
        //location
        region: 'Middle Africa',
        country: 'Central African Republic',
        admin1: 'Ouham',
        admin2: 'Batangafo',
        admin3: 'Bd',
        location: 'Mbali',
        latitude: '7.2113',
        longitude: '17.6704',
        //source
        source: 'Reseau des Journalistes de RCA',
        source_scale: 'Subnational-International',
        notes: 'Ex-Seleka and Fulani attack Mbali village, killing five.',
      }
      ```
    - *visualization*:
      - global overview, 3D map
      - analysis: TBD

  2. [Live News Feed](https://syria.liveuamap.com/)
    - *Retrieval*: [API](https://a.liveuamap.com/api?a=mpts&count=20&key=88a649f99bb136f5ef37d1c7e737932f)
    - *sample data(exclude irrelevant filed)*:
    ```json
    {
      "videocode": "",
      "videotype": null,
      "resid": 62,
      "name": "No decision on &quot;absolute truce&quot; - OSCE rep. Martin Sajdik",
      "video": "",
      "id": 21622240,
      "time": "8 hour ago",
      "pics": [],
      "timestamp": 1519842540,
      "source": "https://twitter.com/qhacomua/status/968916017769582593",
      "picpath": "https://a.liveuamap.com/images/is14/speech_white.png",
      "status_id": 0,
      "svimg": "speech-5",
      "resource": 0,
      "type_id": 1,
      "lat": "53.90285",
      "lng": "27.5598",
      "link": "http://liveuamap.com/en/2018/28-february-no-decision-on-absolute-truce--osce-rep-martin",
      "picture": "",
      "otherregions": "[{\"name\":\"Minsk Monitor\",\"link\":\"https:\\/\\/minskmonitor.liveuamap.com\",\"id\":62}]",
      "city": null,
      "img_share": "https://a.liveuamap.com/pics/2018/02/28/21622240_app.jpg",
      "location": "Minsk",
      "points": "",
      "viaSource": "qhacomua",
      "runway": false
    }
    ```
    - *visualization*:
      - Global overview, additional layer on map, mapping only last 24 hour's data
      - Objective: (let audience understand wars, conflicts are still happening as we speak)


## Chapter 2 - The tragedy never Fade Away (missing/death along the road, what happened post 2016)

### Data Sources
  1. [Missing/Death along the road - The Migrant Files](https://docs.google.com/spreadsheets/d/1YNqIzyQfEn4i_be2GGWESnG2Q80E_fLASffsXdCOftI/edit?usp=sharing)
  |
  [Missing/Death along the road - Missingmigrants, IOM](http://missingmigrants.iom.int/downloads)
    - *Size*: ~5Mb
    - *Total data points*: ~6,000
    - *Timeframe*: __2010__ to __2018__ (truncated)
    - *Scale*: EURO, Mid-East, Mediterranean, Africa
    - *Summary*:
      1. Migrant Files data
        ```json
        year of 2000
        total data record: 269
        death & missing in Total: 991
        ________________
        year of 2001
        total data record: 199
        death & missing in Total: 962
        ________________
        year of 2002
        total data record: 214
        death & missing in Total: 1219
        ________________
        year of 2003
        total data record: 209
        death & missing in Total: 1750
        ________________
        year of 2004
        total data record: 245
        death & missing in Total: 1497
        ________________
        year of 2005
        total data record: 184
        death & missing in Total: 1475
        ________________
        year of 2006
        total data record: 253
        death & missing in Total: 2424
        ________________
        year of 2007
        total data record: 284
        death & missing in Total: 2809
        ________________
        year of 2008
        total data record: 312
        death & missing in Total: 2863
        ________________
        year of 2009
        total data record: 163
        death & missing in Total: 1959
        ________________
        year of 2010
        total data record: 111
        death & missing in Total: 382
        ________________
        year of 2011
        total data record: 161
        death & missing in Total: 4255
        ________________
        year of 2012
        total data record: 106
        death & missing in Total: 926
        ________________
        year of 2013
        total data record: 50
        death & missing in Total: 752
        ________________
        year of 2014
        total data record: 91
        death & missing in Total: 3537
        ________________
        year of 2015
        total data record: 195
        death & missing in Total: 4008
        ________________
        year of 2016
        total data record: 145
        death & missing in Total: 3050
        ________________
        ```
      2. Missing Migrants Data
        ```json
        Year of 2014
        total records: 244
        death & missing in Total: 5285
        ________________
        Year of 2015
        total records: 804
        death & missing in Total: 6281
        ________________
        Year of 2016
        total records: 1240
        death & missing in Total: 7935
        ________________
        Year of 2017
        total records: 1168
        death & missing in Total: 6020
        ________________
        Year of 2018
        total records: 78
        death & missing in Total: 637
        ________________
        ```

    - *Sample data*:
      1. Missingmigrants
        ```json
        {
          "Web ID": "39205",
          "Region of Incident": "Caribbean",
          "Reported Date": "31-Dec-14",
          "Reported Year": 2014,
          "Reported Month": "Dec",
          "Number Dead": "",
          "Number Missing": "1",
          "Total Dead and Missing": "1",
          "Number of survivors": "",
          "Number of Female": "",
          "Number of Male": "1",
          "Number of Children": "",
          "Cause of death": "Drowning",
          "Location Description": "International waters about 22 miles from Cuban territory.",
          "Information Source": "Miami Herald",
          "Location": "23.644500000000, -80.288100000000",
          "Migrant Route": "",
          "URL": "http://hrld.us/1CdEdJM",
          "UNSD Geographical Grouping": "Caribbean",
          "Verification level": "1"
        }
        ```
      2. Migrant Files
        ```JSON
        {
          "Event_id": "36305",
          "cause_of_death": "drowned",
          "CartoDB_Cause_of_death": "unknown - supposedly exhaustion related death",
          "dataset": "United",
          "date": "2000-09-28T00:00:00Z",
          "quarter": "3Q2000",
          "Date-month": "2000 -- 9",
          "Year": 2000,
          "dead": "0",
          "missing": "0",
          "dead_and_missing": "1",
          "Intent of going to Eur: 1(yes) 0(not confirmed)": "",
          "description": "stowaway, froze to dead in wheelbay of Lufthansa airplane at Frankfurt (D) airport (Sep 28, 2000). From Del Grande's data set (translated): Frankfurt Airport. Found the bodies of two men frozen in undercarriage of a Lufthansa cargo departed from Malaysia (Oct 4, 2000)",
          "location": "frankfurt",
          "latitude": "50.110922",
          "longitude": "8.682127",
          "latitude, longitude": "50.110922, 8.682127",
          "Somme Dedoublement": "6",
          "name": "Event at Frankfurt on Sep 28, 2000",
          "route (Frontex)": "",
          "source": "taz/IRR/ARI/BBC",
          "source_url": "http://news.bbc.co.uk/2/hi/asia-pacific/956274.stm"
        }
        ```
    - *visualization*:
      - visualize in conjunction with Frontex defined Route & Price paid to the human smuggler by refugees.

  2. [Frontex Route Data](http://frontex.europa.eu/trends-and-routes/migratory-routes-map/) | [Frontex report](http://frontex.europa.eu/publications/?c=risk-analysis)
    - *Route*:
      1. Western African route,
      2. Western Mediterranean route,
      3. Central Mediterranean route,
      4. Apulia and Calabria route,
      5. Circular route from Albania to Greece,
      6. Western Balkan route,
      7. Eastern Mediterranean route,
      8. Eastern Borders route
    - *Sample data*:
    ```JSON
    {
      "Route":"Black Sea",
      "RouteType": "Sea",
      "num": 1000  
    }
    ```
  3. [Flee from the home - Price paid by refugees to human smuggler](https://docs.google.com/spreadsheets/d/1cynO8lp6crS4p9kJZUqYUigEB15F2cAwGm7aD9cwoZU/edit#gid=779131653)

  ## Chapter 3 - Is there's life out there?

  ### Data Sources
    1. [Refugee stock](https://migrationdataportal.org/?t=2016&i=refug_host&cm49=250) | [displacement Tracking Matrix](https://displacement.iom.int/)
      - *Timeframe*: __2010__ to __2018__
      - *Scale*: Africa, Mid-East, Asia
      - data field: refugee num by country, child refugee rate, resettlement rate, refugee policy, refugee num breakdown by city.
