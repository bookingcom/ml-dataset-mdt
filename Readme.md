## Intro
----------------------
Booking.com provides a unique dataset based on millions of real anonymized bookings to encourage the research on sequential recommendation problems.
Many travelers go on trips which include more than one destination. Our mission at Booking.com is to make it easier for everyone to experience the world, and we can help to do that by providing real-time recommendations for what their next in-trip destination will be. By making accurate predictions, we help deliver a frictionless trip planning experience.
The main challenge is to use a dataset based on millions of real anonymized accommodation reservations to come up with a strategy for making the best recommendation for their next destination in real-time.

![Multi-Destination Trip recommendation bar at booking.com](https://github.com/bookingcom/ml-dataset-mdt/blob/main/mlt_example.jpg)

## Dataset
-------------------
The training dataset consists of over a million (1,166,835) of anonymized hotel reservations, based on real data, with the following features:
- user_id - User ID
- checkin - Reservation check-in date
- checkout - Reservation check-out date- created_date - Date when the reservation was made
- affiliate_id - An anonymized ID of affiliate channels where the booker came from (e.g. direct, some third party referrals, paid search engine, etc.)
- device_class - desktop/mobile
- booker_country - Country from which the reservation was made (anonymized)
- hotel_country - Country of the hotel (anonymized)
- city_id - city_id of the hotel's city (anonymized)
- utrip_id - Unique identification of user's trip (a group of multi-destinations bookings within the same trip).

Each reservation is a part of a customer's trip (identified by utrip_id) which includes consecutive reservations. 
The evaluation dataset is constructed similarly (378,667 reservations), however the city_id (and the country) of the final reservation of each trip is concealed and requires a prediction.



## Citing
----------------------
Booking.com Multi-Destination Trips Dataset is published as a [resource paper at SIGIR '21](https://doi.org/10.1145/3404835.3463240). Please refer to dataset in research publications in the following format:

*Dmitri Goldenberg and Pavel Levin. 2021. Booking.com Multi-Destination Trips Dataset. In Proceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval (SIGIR ’21), July 11–15, 2021, Virtual Event, Canada.* 

#### BibTex:
```
@inproceedings{goldenberg2021dataset,
 author =    {Goldenberg, Dmitri  and Levin, Pavel},
 title =     {Booking.com Multi-Destination Trips Dataset},
 booktitle = {Proceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval (SIGIR ’21)},
 year =      {2021},
 doi  =      {10.1145/3404835.3463240}}
```

For more details, please refer to [Booking.com challenge website](https://www.bookingchallenge.com/) and the [Booking.ai blog](https://booking.ai/).



## Attachments
----------------------
- train_set.csv - Training dataset
- test_set.csv - Validation test set data (with a concealed last destination) as used in Booking.com WSDM WebTour challenge
- ground_truth.csv - The true values of the test set
- submission.csv - an example submission for the test data
- evaluation_demo.ipynb - a Jupyter notebook exampling train set loading, submission generation for test set and evaluation function


## Terms and Conditions
----------------------
- The dataset is a property of Booking.com and may not be reused for commercial purposes.
- The dataset may not be used in a manner that is harmful or competitive in nature with Booking.com or Booking Holdings.
- The dataset may not be used in any manner or for any purpose that may violate any law or regulation.
