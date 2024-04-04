# AirBnB MongoDB Analysis

## Data Set Details
I got my data set from [AirBnB listings data]("https://insideairbnb.com/get-the-data/")
And the original data file is in csv format.

Here is my raw data.
| id     | listing_url                            | scrape_id    | last_scraped | source       | name                                                          | description                                                                                                                                                           | neighborhood_overview                                              | picture_url                                                             | host_id | host_url                            | host_name | host_since | host_location     | host_about                                                                                                                                                                                                                                        | host_response_time | host_response_rate | host_acceptance_rate | host_is_superhost | host_thumbnail_url                                                    | host_picture_url                                                       | host_neighbourhood | host_listings_count | host_total_listings_count | host_verifications        | host_has_profile_pic | host_identity_verified | neighbourhood | neighbourhood_cleansed | neighbourhood_group_cleansed | latitude | longitude | property_type       | room_type     | accommodates | bathrooms | bathrooms_text | bedrooms | beds | amenities                                                       | price     | minimum_nights | maximum_nights | minimum_minimum_nights | maximum_minimum_nights | minimum_maximum_nights | maximum_maximum_nights | minimum_nights_avg_ntm | maximum_nights_avg_ntm | calendar_updated | has_availability | availability_30 | availability_60 | availability_90 | availability_365 | calendar_last_scraped | number_of_reviews | number_of_reviews_ltm | number_of_reviews_l30d | first_review | last_review | review_scores_rating | review_scores_accuracy | review_scores_cleanliness | review_scores_checkin | review_scores_communication | review_scores_location | review_scores_value | license | instant_bookable | calculated_host_listings_count | calculated_host_listings_count_entire_homes | calculated_host_listings_count_private_rooms | calculated_host_listings_count_shared_rooms | reviews_per_month |
|--------|----------------------------------------|--------------|--------------|--------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|---------|-------------------------------------|-----------|------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|--------------------|----------------------|--------------------|----------------------------------------------------------------------|------------------------------------------------------------------------|--------------------|----------------------|--------------------------|---------------------------|---------------------|------------------------|---------------|-----------------------|-----------------------------|----------|-----------|--------------------|---------------|--------------|-----------|----------------|----------|------|-----------------------------------------------------------------|-----------|----------------|----------------|------------------------|------------------------|------------------------|------------------------|------------------------|---------------------|------------------|-----------------|-----------------|-----------------|-----------------|------------------------|--------------------|------------------------|------------------------|--------------|-------------|-----------------|-----------------|-----------------|-----------------|------------------------|-------------------|------------------------|------------------------|--------------|-------------|----------------------|------------------------------------------|------------------------------------------|------------------------------------------|--------------------|
| 17891  | https://www.airbnb.com/rooms/17891     | 2.02312E+13  | 12/21/2023   | previous scrape | Rental unit in Hong Kong Island · ★4.76 · Studio · 1 bed · 1 bath |  |Best neighborhood in Hong Kong! A mix of old and new.                                                                                                                  | https://a0.muscache.com/pictures/119686/6ced58c4_original.jpg  | 69063  | https://www.airbnb.com/users/show/69063 | Candace   | 1/9/2010   | Los Angeles, CA   | Hi, my name is Candace Campos...  | N/A                | N/A                | N/A                  | f                  | https://a0.muscache.com/im/pictures/user/b439cf98-b81c-4555-bb1c-384cf45fe320.jpg?aki_policy=profile_small  | https://a0.muscache.com/im/pictures/user/b439cf98-b81c-4555-bb1c-384cf45fe320.jpg?aki_policy=profile_x_medium  | Sheung Wan         | 1                    | 2                        | ['phone', 'work_email'] | t                   | t                      | Hong Kong Island | Central & Western     |                           | 22.28327 | 114.14988 | Entire rental unit | Entire home/apt | 3            |           | 1 bath         |        |  1     | []                                                              |         |     60           |            365    | 60                      | 60                      | 365                     | 365                     | 60                      | 365                  |              |               | 0               | 0               | 0          |0     | 12/21/2023             | 73                 | 0                      | 0                      | 4/23/2010    | 11/29/2017  | 4.76                 | 4.73                   | 4.51                      | 4.92                   | 4.93                          | 4.9                    | 4.66               |          | f               | 1                              | 1                                        | 0                                      | 0                                        | 0.44               |
| 72571  | https://www.airbnb.com/rooms/72571     | 2.02312E+13  | 12/20/2023   | city scrape   | Rental unit in Sheung Wan · ★4.22 · Studio · 1 bed · 1 bath     |         |                                                                                                                                                              | https://a0.muscache.com/pictures/2849554/d226294d_original.jpg  | 304876 | https://www.airbnb.com/users/show/304876 | Brendan   | 11/30/2010 | Hong Kong         | I was born in California and raised in Hong Kong... | within an hour      | 100%               | 99%                  | f                  | https://a0.muscache.com/im/users/304876/profile_pic/1359947330/original.jpg?aki_policy=profile_small  | https://a0.muscache.com/im/users/304876/profile_pic/1359947330/original.jpg?aki_policy=profile_x_medium  | Sheung Wan         | 10                   | 58                       | ['email', 'phone']        | t                   | t                      |               | Central & Western     |                           | 22.28463 | 114.15054 | Entire rental unit | Entire home/apt | 2            |           | 1 bath         |          |   1   | []                                                              | $482.00   | 28             | 1125           | 28                     | 28                     | 1125                     | 1125                     | 28                     | 1125                 |            | t              | 0              | 0              | 0|0              | 12/20/2023             | 151                | 0                      | 0                      | 2/26/2011    | 3/11/2022   | 4.22                 | 4.04                   | 4.55                      | 4.43                   | 4.51                          | 4.73                   | 4.13               |          | f               | 9                              | 5                                        | 4                                        | 0                                        | 0.97               |
| 132773 | https://www.airbnb.com/rooms/132773    | 2.02312E+13  | 12/21/2023   | city scrape   | Rental unit in Hong Kong Island · ★4.52 · 2 bedrooms · 3 beds · 1 bath | |The Sheung Wan neighbourhood is ever changing and a fantastic mix of "old' and "new" Hong Kong... | https://a0.muscache.com/pictures/36936441/e4c1f31d_original.jpg | 304876 | https://www.airbnb.com/users/show/304876 | Brendan   | 11/30/2010 | Hong Kong         | I was born in California and raised in Hong Kong... | within an hour      | 100%               | 99%                  | f                  | https://a0.muscache.com/im/users/304876/profile_pic/1359947330/original.jpg?aki_policy=profile_small  | https://a0.muscache.com/im/users/304876/profile_pic/1359947330/original.jpg?aki_policy=profile_x_medium  | Sheung Wan         | 10                   | 58                       | ['email', 'phone']        | t                   | t                      | Hong Kong Island | Central & Western     |                           | 22.28921 | 114.14325 | Entire rental unit | Entire home/apt | 6            |           | 1 bath         |         |  3    | []                                                              | $1,475.00 | 5              | 365            | 5                      | 5                      | 365                      | 365                      | 5                      | 365                   |                 | t              | 0               | 0               | 0|0               | 12/21/2023             | 247                | 24                     | 3                      | 7/19/2011    | 12/3/2023   | 4.52                 | 4.49                   | 4.7                       | 4.6                    | 4.67                          | 4.43                   | 4.41               |          | f               | 9                              | 5                                        | 4                                        | 0                                        | 1.63               |
| 163664 | https://www.airbnb.com/rooms/163664    | 2.02312E+13  | 12/20/2023   | city scrape   | Rental unit in Sheung Wan · ★4.28 · 2 bedrooms · 3 beds · 1 bath | |Fantastic traditional Hong Kong neighborhood with lots of history at every street alley and corner...                                                          | https://a0.muscache.com/pictures/15184030/8d06b40b_original.jpg | 304876 | https://www.airbnb.com/users/show/304876 | Brendan   | 11/30/2010 | Hong Kong         | I was born in California and raised in Hong Kong...| within an hour      | 100%               | 99%                  | f                  | https://a0.muscache.com/im/users/304876/profile_pic/1359947330/original.jpg?aki_policy=profile_small  | https://a0.muscache.com/im/users/304876/profile_pic/1359947330/original.jpg?aki_policy=profile_x_medium  | Sheung Wan         | 10                   | 58                       | ['email', 'phone']        | t                   | t                      | Sheung Wan      | Central & Western     |                           | 22.28494 | 114.14901 | Entire rental unit | Entire home/apt | 6            |           | 1 bath         |         |    3  | []                                                              | $616.00   | 2              | 365            | 2                      | 2                      | 365                      | 365                      | 2                      | 365                   |                | t              | 0               | 0              | 0|0               | 12/20/2023             | 225                | 0                      | 0                      | 8/25/2011    | 2/16/2021   | 4.28                 | 4.24                   | 4.41                      | 4.44                   | 4.58                          | 4.68                   | 4.31               |          | f               | 9                              | 5                                        | 4                                        | 0                                        | 1.5                |
| 163742 | https://www.airbnb.com/rooms/163742    | 2.02312E+13  | 12/21/2023   | city scrape   | Rental unit in Sheung Wan · ★4.35 · 2 bedrooms · 3 beds · 1 bath | |Fantastic traditional Hong Kong neighborhood with lots of history at every street alley and corner...                                   | https://a0.muscache.com/pictures/15195137/ff7e10d7_original.jpg | 304876 | https://www.airbnb.com/users/show/304876 | Brendan   | 11/30/2010 | Hong Kong         | I was born in California and raised in Hong Kong...| within an hour      | 100%               | 99%                  | f                  | https://a0.muscache.com/im/users/304876/profile_pic/1359947330/original.jpg?aki_policy=profile_small  | https://a0.muscache.com/im/users/304876/profile_pic/1359947330/original.jpg?aki_policy=profile_x_medium  | Sheung Wan         | 10                   | 58                       | ['email', 'phone']        | t                   | t                      | Sheung Wan      | Central & Western     |                           | 22.28657 | 114.14889 | Entire rental unit | Entire home/apt | 6            |           | 1 bath         |         |  3    | []                                                              | $1,210.00 | 4              | 365            | 4                      | 4                      | 365                     | 365                      | 4                      | 365                   |                 |   t             | 0       |0        | 0               | 0               | 12/21/2023             | 244                | 10                     | 0                      | 8/11/2011    | 11/20/2023  | 4.35                 | 4.26                   | 4.51                      | 4.52                   | 4.59                          | 4.62                   | 4.31               |          | f               | 9                              | 5                                        | 4                                        | 0                                        | 1.62               |


## Analysis
1. Show exactly two documents from the listings collection in any order
 
 I choose to present the data in ascending order of "_id" field.

 Command
```
db.listings.find().sort({_id: 1}).limit(2)
```

Result
```
{
    _id: ObjectId('660db9f8b6515eb20577a8d0'),
    id: Long('712914322433199115'),
    listing_url: 'https://www.airbnb.com/rooms/712914322433199115',
    scrape_id: Long('20240322023511'),
    last_scraped: '2024-03-22',
    source: 'city scrape',
    name: 'Welcome 1-bedroom available. Free parking & Wi-Fi',
    description: 'Single room available in family home. Bus route 5 minute walk away to city centre. Close to aerport.',
    neighborhood_overview: '',
    picture_url: 'https://a0.muscache.com/pictures/4c044921-f6fd-4f84-a313-51cd9b3fb1b5.jpg',
    host_id: 89156390,
    host_url: 'https://www.airbnb.com/users/show/89156390',
    host_name: 'Teresa',
    host_since: '2016-08-10',
    host_location: 'County Dublin, Ireland',
    host_about: '',
    host_response_time: 'within an hour',
    host_response_rate: '90%',
    host_acceptance_rate: '73%',
    host_is_superhost: 'f',
    host_thumbnail_url: 'https://a0.muscache.com/im/pictures/user/c338892a-7813-4be6-8763-78548b463cf0.jpg?aki_policy=profile_small',
    host_picture_url: 'https://a0.muscache.com/im/pictures/user/c338892a-7813-4be6-8763-78548b463cf0.jpg?aki_policy=profile_x_medium',
    host_neighbourhood: '',
    host_listings_count: 2,
    host_total_listings_count: 2,
    host_verifications: "['email', 'phone']",
    host_has_profile_pic: 't',
    host_identity_verified: 't',
    neighbourhood: '',
    neighbourhood_cleansed: 'Fingal',
    neighbourhood_group_cleansed: '',
    latitude: 53.45891,
    longitude: -6.22553,
    property_type: 'Private room in casa particular',
    room_type: 'Private room',
    accommodates: 1,
    bathrooms: 1,
    bathrooms_text: '1 shared bath',
    bedrooms: 1,
    beds: 1,
    amenities: '["Free parking on premises", "Central heating", "Hair dryer", "Essentials", "Wifi"]',
    price: '$60.00',
    minimum_nights: 1,
    maximum_nights: 2,
    minimum_minimum_nights: 1,
    maximum_minimum_nights: 1,
    minimum_maximum_nights: 2,
    maximum_maximum_nights: 2,
    minimum_nights_avg_ntm: 1,
    maximum_nights_avg_ntm: 2,
    calendar_updated: '',
    has_availability: 't',
    availability_30: 29,
    availability_60: 59,
    availability_90: 87,
    availability_365: 87,
    calendar_last_scraped: '2024-03-22',
    number_of_reviews: 61,
    number_of_reviews_ltm: 45,
    number_of_reviews_l30d: 0,
    first_review: '2022-09-13',
    last_review: '2024-02-16',
    review_scores_rating: 4.8,
    review_scores_accuracy: 4.92,
    review_scores_cleanliness: 4.85,
    review_scores_checkin: 4.74,
    review_scores_communication: 4.79,
    review_scores_location: 4.93,
    review_scores_value: 4.7,
    license: '',
    instant_bookable: 'f',
    calculated_host_listings_count: 2,
    calculated_host_listings_count_entire_homes: 0,
    calculated_host_listings_count_private_rooms: 2,
    calculated_host_listings_count_shared_rooms: 0,
    reviews_per_month: 3.29
},
{
    _id: ObjectId('660db9f8b6515eb20577a8d1'),
    id: 1729959,
    listing_url: 'https://www.airbnb.com/rooms/1729959',
    scrape_id: Long('20240322023511'),
    last_scraped: '2024-03-22',
    source: 'city scrape',
    name: "Kim's House",
    description: "Our home is bright and family friendly with a good space downstairs and a main bedroom and 2 children's bedrooms (for 3 kids) upstairs.",
    neighborhood_overview: '',
    picture_url: 'https://a0.muscache.com/pictures/miso/Hosting-1729959/original/91cc6582-d962-4965-993c-fd03f07cbb0a.jpeg',
    host_id: 9115187,
    host_url: 'https://www.airbnb.com/users/show/9115187',
    host_name: 'Kim',
    host_since: '2013-09-29',
    host_location: 'Dublin, Ireland',
    host_about: "I'm a friendly, honest, easygoing person who loves to travel and experience what life has to offer. Myself and my husband met in South America whilst volunteering, and we have had many journeys around the world since, including working in North Africa and taking the train across Russia. Nowadays though, life is different, we have 3 small children so we rarely get past the front door without a bit of effort. That's why we would like to make our home (or spare room) available to people who want to explore Dublin - we can get a bit of the travelling experience from our visitors! We both like movies and books, box sets of Sopranos, The Wire (and a little bit of Downton just for me) and, of course, Guinness. We are vegetarians, but wouldn't mind if a guest wanted to cook meat, and we love eating out or creating our own feasts whenever we can. I hope to provide a guest with a welcoming atmosphere, interesting chat and good ideas about how to get the most out of their stay in Dublin, whatever their age or interests.",
    host_response_time: 'within an hour',
    host_response_rate: '100%',
    host_acceptance_rate: '83%',
    host_is_superhost: 'f',
    host_thumbnail_url: 'https://a0.muscache.com/im/pictures/user/52e2e63d-9685-41f4-b94c-25ad38955cc3.jpg?aki_policy=profile_small',
    host_picture_url: 'https://a0.muscache.com/im/pictures/user/52e2e63d-9685-41f4-b94c-25ad38955cc3.jpg?aki_policy=profile_x_medium',
    host_neighbourhood: 'Dundrum',
    host_listings_count: 1,
    host_total_listings_count: 3,
    host_verifications: "['email', 'phone']",
    host_has_profile_pic: 't',
    host_identity_verified: 't',
    neighbourhood: '',
    neighbourhood_cleansed: 'Dn Laoghaire-Rathdown',
    neighbourhood_group_cleansed: '',
    latitude: 53.3065,
    longitude: -6.24719,
    property_type: 'Entire home',
    room_type: 'Entire home/apt',
    accommodates: 6,
    bathrooms: 1.5,
    bathrooms_text: '1.5 baths',
    bedrooms: 3,
    beds: 5,
    amenities: '["Heating", "Children\\u2019s books and toys for ages 5-10 years old", "Kitchen", "Free parking on premises", "Washer", "Bathtub", "Smoke alarm", "Wifi", "Host greets you", "TV with standard cable"]',
    price: '$215.00',
    minimum_nights: 5,
    maximum_nights: 1125,
    minimum_minimum_nights: 5,
    maximum_minimum_nights: 5,
    minimum_maximum_nights: 1125,
    maximum_maximum_nights: 1125,
    minimum_nights_avg_ntm: 5,
    maximum_nights_avg_ntm: 1125,
    calendar_updated: '',
    has_availability: 't',
    availability_30: 0,
    availability_60: 0,
    availability_90: 0,
    availability_365: 9,
    calendar_last_scraped: '2024-03-22',
    number_of_reviews: 7,
    number_of_reviews_ltm: 3,
    number_of_reviews_l30d: 0,
    first_review: '2015-04-05',
    last_review: '2023-07-07',
    review_scores_rating: 4.86,
    review_scores_accuracy: 4.71,
    review_scores_cleanliness: 4.14,
    review_scores_checkin: 5,
    review_scores_communication: 5,
    review_scores_location: 4.86,
    review_scores_value: 4.71,
    license: '',
    instant_bookable: 'f',
    calculated_host_listings_count: 1,
    calculated_host_listings_count_entire_homes: 1,
    calculated_host_listings_count_private_rooms: 0,
    calculated_host_listings_count_shared_rooms: 0,
    reviews_per_month: 0.06
}
```

2. Show exactly 10 documents in any order, but "prettyprint" in easier to read format, using the pretty() function

Command
```
db.listings.find().limit(10).forEach(function(doc) {printjson(doc)});
```

Result
```
{
_id: ObjectId('660db9f8b6515eb20577a8d0'),
  id: Long('712914322433199115'),
  listing_url: 'https://www.airbnb.com/rooms/712914322433199115',
  scrape_id: Long('20240322023511'),
  last_scraped: '2024-03-22',
  source: 'city scrape',
  name: 'Welcome 1-bedroom available. Free parking & Wi-Fi',
  description: 'Single room available in family home. Bus route 5 minute walk away to city centre. Close to aerport.',
  neighborhood_overview: '',
  picture_url: 'https://a0.muscache.com/pictures/4c044921-f6fd-4f84-a313-51cd9b3fb1b5.jpg',
  host_id: 89156390,
  host_url: 'https://www.airbnb.com/users/show/89156390',
  host_name: 'Teresa',
  host_since: '2016-08-10',
  host_location: 'County Dublin, Ireland',
  host_about: '',
  host_response_time: 'within an hour',
  host_response_rate: '90%',
  host_acceptance_rate: '73%',
  host_is_superhost: 'f',
  host_thumbnail_url: 'https://a0.muscache.com/im/pictures/user/c338892a-7813-4be6-8763-78548b463cf0.jpg?aki_policy=profile_small',
  host_picture_url: 'https://a0.muscache.com/im/pictures/user/c338892a-7813-4be6-8763-78548b463cf0.jpg?aki_policy=profile_x_medium',
  host_neighbourhood: '',
  host_listings_count: 2,
  host_total_listings_count: 2,
  host_verifications: "['email', 'phone']",
  host_has_profile_pic: 't',
  host_identity_verified: 't',
  neighbourhood: '',
  neighbourhood_cleansed: 'Fingal',
  neighbourhood_group_cleansed: '',
  latitude: 53.45891,
  longitude: -6.22553,
  property_type: 'Private room in casa particular',
  room_type: 'Private room',
  accommodates: 1,
  bathrooms: 1,
  bathrooms_text: '1 shared bath',
  bedrooms: 1,
  beds: 1,
  amenities: '["Free parking on premises", "Central heating", "Hair dryer", "Essentials", "Wifi"]',
  price: '$60.00',
  minimum_nights: 1,
  maximum_nights: 2,
  minimum_minimum_nights: 1,
  maximum_minimum_nights: 1,
  minimum_maximum_nights: 2,
  maximum_maximum_nights: 2,
  minimum_nights_avg_ntm: 1,
  maximum_nights_avg_ntm: 2,
  calendar_updated: '',
  has_availability: 't',
  availability_30: 29,
  availability_60: 59,
  availability_90: 87,
  availability_365: 87,
  calendar_last_scraped: '2024-03-22',
  number_of_reviews: 61,
  number_of_reviews_ltm: 45,
  number_of_reviews_l30d: 0,
  first_review: '2022-09-13',
  last_review: '2024-02-16',
  review_scores_rating: 4.8,
  review_scores_accuracy: 4.92,
  review_scores_cleanliness: 4.85,
  review_scores_checkin: 4.74,
  review_scores_communication: 4.79,
  review_scores_location: 4.93,
  review_scores_value: 4.7,
  license: '',
  instant_bookable: 'f',
  calculated_host_listings_count: 2,
  calculated_host_listings_count_entire_homes: 0,
  calculated_host_listings_count_private_rooms: 2,
  calculated_host_listings_count_shared_rooms: 0,
  reviews_per_month: 3.29
}
{
  _id: ObjectId('660db9f8b6515eb20577a8d1'),
  id: 1729959,
  listing_url: 'https://www.airbnb.com/rooms/1729959',
  scrape_id: Long('20240322023511'),
  last_scraped: '2024-03-22',
  source: 'city scrape',
  name: "Kim's House",
  description: "Our home is bright and family friendly with a good space downstairs and a main bedroom and 2 children's bedrooms (for 3 kids) upstairs.",
  neighborhood_overview: '',
  picture_url: 'https://a0.muscache.com/pictures/miso/Hosting-1729959/original/91cc6582-d962-4965-993c-fd03f07cbb0a.jpeg',
  host_id: 9115187,
  host_url: 'https://www.airbnb.com/users/show/9115187',
  host_name: 'Kim',
  host_since: '2013-09-29',
  host_location: 'Dublin, Ireland',
  host_about: "I'm a friendly, honest, easygoing person who loves to travel and experience what life has to offer. Myself and my husband met in South America whilst volunteering, and we have had many journeys around the world since, including working in North Africa and taking the train across Russia. Nowadays though, life is different, we have 3 small children so we rarely get past the front door without a bit of effort. That's why we would like to make our home (or spare room) available to people who want to explore Dublin - we can get a bit of the travelling experience from our visitors! We both like movies and books, box sets of Sopranos, The Wire (and a little bit of Downton just for me) and, of course, Guinness. We are vegetarians, but wouldn't mind if a guest wanted to cook meat, and we love eating out or creating our own feasts whenever we can. I hope to provide a guest with a welcoming atmosphere, interesting chat and good ideas about how to get the most out of their stay in Dublin, whatever their age or interests.",
  host_response_time: 'within an hour',
  host_response_rate: '100%',
  host_acceptance_rate: '83%',
  host_is_superhost: 'f',
  host_thumbnail_url: 'https://a0.muscache.com/im/pictures/user/52e2e63d-9685-41f4-b94c-25ad38955cc3.jpg?aki_policy=profile_small',
  host_picture_url: 'https://a0.muscache.com/im/pictures/user/52e2e63d-9685-41f4-b94c-25ad38955cc3.jpg?aki_policy=profile_x_medium',
  host_neighbourhood: 'Dundrum',
  host_listings_count: 1,
  host_total_listings_count: 3,
  host_verifications: "['email', 'phone']",
  host_has_profile_pic: 't',
  host_identity_verified: 't',
  neighbourhood: '',
  neighbourhood_cleansed: 'Dn Laoghaire-Rathdown',
  neighbourhood_group_cleansed: '',
  latitude: 53.3065,
  longitude: -6.24719,
  property_type: 'Entire home',
  room_type: 'Entire home/apt',
  accommodates: 6,
  bathrooms: 1.5,
  bathrooms_text: '1.5 baths',
  bedrooms: 3,
  beds: 5,
  amenities: '["Heating", "Children\\u2019s books and toys for ages 5-10 years old", "Kitchen", "Free parking on premises", "Washer", "Bathtub", "Smoke alarm", "Wifi", "Host greets you", "TV with standard cable"]',
  price: '$215.00',
  minimum_nights: 5,
  maximum_nights: 1125,
  minimum_minimum_nights: 5,
  maximum_minimum_nights: 5,
  minimum_maximum_nights: 1125,
  maximum_maximum_nights: 1125,
  minimum_nights_avg_ntm: 5,
  maximum_nights_avg_ntm: 1125,
  calendar_updated: '',
  has_availability: 't',
  availability_30: 0,
  availability_60: 0,
  availability_90: 0,
  availability_365: 9,
  calendar_last_scraped: '2024-03-22',
  number_of_reviews: 7,
  number_of_reviews_ltm: 3,
  number_of_reviews_l30d: 0,
  first_review: '2015-04-05',
  last_review: '2023-07-07',
  review_scores_rating: 4.86,
  review_scores_accuracy: 4.71,
  review_scores_cleanliness: 4.14,
  review_scores_checkin: 5,
  review_scores_communication: 5,
  review_scores_location: 4.86,
  review_scores_value: 4.71,
  license: '',
  instant_bookable: 'f',
  calculated_host_listings_count: 1,
  calculated_host_listings_count_entire_homes: 1,
  calculated_host_listings_count_private_rooms: 0,
  calculated_host_listings_count_shared_rooms: 0,
  reviews_per_month: 0.06
}
{
  _id: ObjectId('660db9f8b6515eb20577a8d2'),
  id: Long('836161818988851736'),
  listing_url: 'https://www.airbnb.com/rooms/836161818988851736',
  scrape_id: Long('20240322023511'),
  last_scraped: '2024-03-22',
  source: 'city scrape',
  name: 'Private Room Beautiful Townhouse',
  description: 'Private room in beautiful Victorian-style townhouse in the City Centre. Right beside Merrion Square & 10 minutes walking to Grafton St and St. Stephens Green, you will find everything accessible while still having a bit of peace and quiet. The bedroom has a super-king bed, working space, and ensuite (shower included). My roommate, a lovely late 20s Italian guy working in Finance, occupies the other room, he will assist you with your stay and make you feel comfortable.',
  neighborhood_overview: '',
  picture_url: 'https://a0.muscache.com/pictures/miso/Hosting-836161818988851736/original/7ebd1615-f0be-4743-a06c-c2abd3c81322.jpeg',
  host_id: 202741475,
  host_url: 'https://www.airbnb.com/users/show/202741475',
  host_name: 'Gabriella',
  host_since: '2018-07-16',
  host_location: 'Dublin, Ireland',
  host_about: '',
  host_response_time: 'within a few hours',
  host_response_rate: '100%',
  host_acceptance_rate: '54%',
  host_is_superhost: 'f',
  host_thumbnail_url: 'https://a0.muscache.com/im/pictures/user/User-202741475/original/ee5f9b55-a253-47a7-8efa-7f63bc828059.jpeg?aki_policy=profile_small',
  host_picture_url: 'https://a0.muscache.com/im/pictures/user/User-202741475/original/ee5f9b55-a253-47a7-8efa-7f63bc828059.jpeg?aki_policy=profile_x_medium',
  host_neighbourhood: '',
  host_listings_count: 2,
  host_total_listings_count: 2,
  host_verifications: "['email', 'phone']",
  host_has_profile_pic: 't',
  host_identity_verified: 't',
  neighbourhood: '',
  neighbourhood_cleansed: 'Dublin City',
  neighbourhood_group_cleansed: '',
  latitude: 53.34168825054963,
  longitude: -6.248907026250597,
  property_type: 'Private room in rental unit',
  room_type: 'Private room',
  accommodates: 1,
  bathrooms: 1.5,
  bathrooms_text: '1.5 baths',
  bedrooms: 1,
  beds: 1,
  amenities: '["Indoor fireplace", "Long term stays allowed", "Body soap", "Double oven", "Conditioner", "Shower gel", "Hot water kettle", "Dedicated workspace", "TV with Amazon Prime Video, Netflix", "Refrigerator", "Drying rack for clothing", "Host greets you", "Cooking basics", "Kitchen", "Hangers", "Washer", "Dining table", "Hot water", "Smoke alarm", "Wifi", "Cleaning products", "Luggage dropoff allowed", "Extra pillows and blankets", "Free dryer \\u2013 In unit", "Microwave", "Central heating", "Shampoo", "Dishwasher", "Dishes and silverware", "Essentials", "Freezer", "Clothing storage: closet, wardrobe, and dresser", "Outdoor dining area", "Fire extinguisher"]',
  price: '$90.00',
  minimum_nights: 1,
  maximum_nights: 365,
  minimum_minimum_nights: 1,
  maximum_minimum_nights: 2,
  minimum_maximum_nights: 365,
  maximum_maximum_nights: 365,
  minimum_nights_avg_ntm: 1.9,
  maximum_nights_avg_ntm: 365,
  calendar_updated: '',
  has_availability: 't',
  availability_30: 8,
  availability_60: 8,
  availability_90: 8,
  availability_365: 8,
  calendar_last_scraped: '2024-03-22',
  number_of_reviews: 5,
  number_of_reviews_ltm: 5,
  number_of_reviews_l30d: 2,
  first_review: '2023-06-25',
  last_review: '2024-03-16',
  review_scores_rating: 4.4,
  review_scores_accuracy: 4.6,
  review_scores_cleanliness: 4.4,
  review_scores_checkin: 5,
  review_scores_communication: 5,
  review_scores_location: 5,
  review_scores_value: 4.8,
  license: '',
  instant_bookable: 'f',
  calculated_host_listings_count: 1,
  calculated_host_listings_count_entire_homes: 0,
  calculated_host_listings_count_private_rooms: 1,
  calculated_host_listings_count_shared_rooms: 0,
  reviews_per_month: 0.55
}
```

3. Choose two hosts (by reffering to their host_id values) who are superhosts (available in the host_is_superhost field), and show all of the listings offered by both of the two hosts
I choose 445632319 and 55276705 with "t" in the column of "host_is_superhost".

Command
```
db.listings.find({
    $and: [
        { $or: [
            { host_id: 445632319 },
            { host_id: 55276705 }
        ]},
        { host_is_superhost: 't' }
    ]
}, {
    name: 1,
    price: 1,
    neighbourhood: 1,
    host_name: 1,
    host_is_superhost: 1,
    _id: 0
})

```

Result
```
 {
    name: 'Bright 1 bed condo near  Dublin City',
    host_name: 'John',
    host_is_superhost: 't',
    neighbourhood: '',
    price: '$105.00'
},
{
    name: '1-Bedroom Apartment in Dublin City Centre',
    host_name: 'Gregory Joseph',
    host_is_superhost: 't',
    neighbourhood: 'Dublin 1, County Dublin, Ireland',
    price: '$150.00'
},
{
    name: 'Central & Spacious City Centre Apt',
    host_name: 'Gregory Joseph',
    host_is_superhost: 't',
    neighbourhood: 'Dublin 1, County Dublin, Ireland',
    price: '$345.00'
}
```
4. Find all the unique host_name values

Command
```
db.listings.distinct("host_name")
```

Result
```
'A',                  'AJ',             
'ADam',
```
5. Find all of the places that have more than 2 beds in a neighborhood of your choice (referred to as either the neighborhood or neighbourhood_group_cleansed fields in the data file), ordered by review_scores_rating descending

Command
```
db.listings.find({
    $and: [
        { $or: [{ neighbourhood: { $ne: "" } }, { neighbourhood_group_cleansed: { $ne: "" } }] },
        { beds: { $gt: 2 } },
        { review_scores_rating: { $ne: "" } }
    ]
}, {
    name: 1,
    beds: 1,
    review_scores_rating: 1,
    price: 1,
    _id: 0
}).sort({ review_scores_rating: -1 }).limit(10)

```

Result
```
{
    name: 'Recently refurbished 4-bedroom home in Sandymount',
    beds: 5,
    price: '$896.00',
    review_scores_rating: 5
  },
  {
    name: 'Modern town house in the heart of Skerries.',
    beds: 3,
    price: '$110.00',
    review_scores_rating: 5
  },
  {
    name: 'Large Georgian house close to Dublin City Center',
    beds: 8,
    price: '$696.00',
    review_scores_rating: 5
  },
```

From the result, people travel with family groups can choose more appropriate house.

6. Show the number of listings per host

Command
```
db.listings.aggregate([
    {
        $group: {
            _id: "$host_id",
            count: { $sum: 1 }
        }
    }
])

```

Result
```
{ _id: 50273422, count: 2 },
{ _id: 46267039, count: 2 },
{ _id: 228263, count: 2 },
```

7. Find the average review_scores_rating per neighborhood, and only show those that are 4 or above, sorted in descending order of rating

Command
```
 db.listings.aggregate([
    {
        $match: {
            "review_scores_rating": { $gte: 4 } 
        }
    },
    {
        $group: {
            _id: "$neighbourhood_cleansed", 
            avgRating: { $avg: "$review_scores_rating" } 
        }
    },
    {
        $match: {
            avgRating: { $gte: 4 } 
        }
    },
    {
        $sort: {
            avgRating: -1 
        }
    }
])
```

Result
```
{ _id: 'Dn Laoghaire-Rathdown', avgRating: 4.859588377723971 },
{ _id: 'Fingal', avgRating: 4.846906779661016 },
{ _id: 'South Dublin', avgRating: 4.8196484375 },
```

From the result, we can conclude which neighborhood provide better accommodation.