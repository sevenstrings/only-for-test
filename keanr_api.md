Keanr api
=======================

### GET /accounts/referral/
response:

*200 (ok)

*format - text

*referral page

### POST /accounts/referral/
>params:

>*referrer - referrer's email

>response:

>* success

>* 201 (created)

>* format: json

>* { }

>* fail

>* 200 (ok)

>* format -text

>* referral page (with error information)

### GET /accounts/user_id/
* response: 
** 200 (ok)
** format: json
** example: {'name': 'Alec Gellis', 'username': 'AG_1234', 'Tagline': 'Living life to the fullest!', 'Interests': '#Biking, #movies, #Cooking, #Traveling', 'birthday': '5-21-1982'; 'gender': 'M', 'gender_interest': 'Female', 'look_for': 'Friendships, Netwroking', 'Relationship_status': 'Single', 'language': 'English, German', 'ethnicity': 'German', 'religion': 'Catholic', 'political_views': 'liberal', 'expertise': '#Product Design, #UI', 'work_education': 'College Graduate'}

### PUT /accounts/profile/
* params: name, username, tagline, birthday(mm-dd-yyyy), interests, gender(m/f), look_for, relationship_status, language, ethnicity, political_view, expertise, work_education. (all optional)
* response: 
** 202 (accepted)
** format: json
** { }

### GET /friends/
* response:
** format: json
** example: [{'name': 'Ke Guan', 'facebook_id': '100000988865835', 'interests_num': '3', 'avg_score': 9.8}, {'name': 'Cindy Angel', 'facebook_id': '100006763179779', 'interests_num': '2', 'avg_score': 9.9}]

### GET /orders/
* response:
*   format: json
*   [{'deal_id': '', ‘deal_url’: ‘’}, {‘deal_id': '', ‘deal_url’: ‘’}, …]

### POST /orders/
* params:
*   i_uid - facebook id list of friends invited
*   b_uid - facebook id list of friends buy for
*   deal_url - deal's url
* response:
*   format: json
*   { }

### GET /invitations/
* response:
*   format: json
*   [{'deal_url': '',
*     'owner': '', 'invitees': [{'name': '', 'status': ''}, ...],
*     'buy_fors': [{'name': '', 'status': ''}, ... ]
*    }, ... ]

### GET /orders/order_id/
* response:
*   format: json
*   {‘deal_url’:’’, 'owner': '', ‘invitees’: [{'name': '', 'status': ''}, …], 'buy_fors': [{'name': '', 'status': ''}, ...]}
