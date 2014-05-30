Keanr api
=======================

##### GET /accounts/referral/

response:
* 200 (ok)
* format - text
* referral page

##### POST /accounts/referral/

params:
* referrer - referrer's email

response:
* success
* 201 (created)
* format: json
* { }
* fail
* 200 (ok)
* format -text
* referral page (with error information)

##### GET /accounts/user_id/

response: 
* 200 (ok)
* format: json
* example: {'name': 'Alec Gellis', 'username': 'AG_1234', 'Tagline': 'Living life to the fullest!', 'Interests': '#Biking, #movies, #Cooking, #Traveling', 'birthday': '5-21-1982'; 'gender': 'M', 'gender_interest': 'Female', 'look_for': 'Friendships, Netwroking', 'Relationship_status': 'Single', 'language': 'English, German', 'ethnicity': 'German', 'religion': 'Catholic', 'political_views': 'liberal', 'expertise': '#Product Design, #UI', 'work_education': 'College Graduate'}

##### PUT /accounts/profile/

params: name, username, tagline, birthday(yyyy-mm-dd), interests, gender(m/f), look_for, relationship_status, language, ethnicity, political_view, expertise, work_education. (all optional)

response: 
* 202 (accepted)
* format: json
* { }

##### GET /friends/

response:
* 200 (ok)
* format: json
* example: [{'name': 'Ke Guan', 'facebook_id': '100000988865835', 'interests_num': '3', 'avg_score': 9.8}, {'name': 'Cindy Angel', 'facebook_id': '100006763179779', 'interests_num': '2', 'avg_score': 9.9}]
* *facebook avatar url: http://graph.facebook.com/<facebook_id>/picture

##### GET /orders/

response:
* 200 (ok)
* format: json
* example: [{'deal_id': 1, ‘deal_url’: ‘https://www.dealflicks.com/theaters/grand-lake-theater/movies/the-wolf-of-wall-street/deals’, 'city': 'Oakland', 'theater': 'grand lake theater', 'movie': 'the wolf of wall street', 'datetime': '2014-05-20T07:30:00-08:00', 'owner': 'Ke Guan'}, …]

##### POST /orders/

params:
* i_uids - facebook id list of friends invited
* b_uids - facebook id list of friends buy for
* deal_url - deal's url
* theater
* movie
* dealflicks_price
* retail_price
* date

response:
* 201 (created) or 400 (bad request)
* format: json
* { }

##### GET /invitations/

response:
* 200 (ok)
* format: json
* example: [{'deal_id': 1, ‘deal_url’: ‘https://www.dealflicks.com/theaters/grand-lake-theater/movies/the-wolf-of-wall-street/deals’, 'city': 'Oakland', 'theater': 'grand lake theater', 'movie': 'the wolf of wall street', 'datetime': '2014-05-20T07:30:00-08:00', 'owner': {'name': 'Ke Guan', 'avatar': 'http://www.keanr.com/11211/avatar.jpg'}}, ...]

##### GET /orders/order_id/

response:
# 200 (ok)
* format: json
* {'deal_id': 1, ‘deal_url’: ‘https://www.dealflicks.com/theaters/grand-lake-theater/movies/the-wolf-of-wall-street/deals’, 'city': 'Oakland', 'theater': 'grand lake theater', 'movie': 'the wolf of wall street', 'datetime': '2014-05-20T07:30:00-08:00', 'owner': 'Ke Guan', 'invitees': [{'name': 'Jim Green', 'status': 'yes'}, {'name': 'Lucy King', 'status': 'no'}], 'buy_fors': [{'name': 'Jack Brown', 'status': ''}]}
