Keanr api
=======================

# GET /accounts/referral/
> response:
>  format - text
>  referral page

# POST /accounts/referral/
> params:
>   referrer - referrer's email
> response:
>   format: json
>   { }

# GET /accounts/user_id/
> response: 
>   format: json
>   {‘name’: ‘’, 'user_name': '', 'birthday': '', ...}


# PUT /accounts/user_id/
> params: name, username, tagline, birthday(mm-dd-yyyy), interests, gender(m/f), look_for, relationship_status, language, ethnicity, political_view, expertise, work_education. (all optional)
> response: 
>   format: json
>   { }

# GET /friends/
> response:
>   format: json
>   [{'name': '', 'facebook_id': '', {'name': '', 'facebook_id': ''}, ...]

# GET /orders/
> response:
>   format: json
>   [{'deal_id': '', ‘deal_url’: ‘’}, {‘deal_id': '', ‘deal_url’: ‘’}, …]

# POST /orders/
> params:
>   i_uid - facebook id list of friends invited
>   b_uid - facebook id list of friends buy for
>   deal_url - deal's url
> response:
>   format: json
>   { }

# GET /invitations/
> response:
>   format: json
>   [{'deal_url': '',
>     'owner': '', 'invitees': [{'name': '', 'status': ''}, ...],
>     'buy_fors': [{'name': '', 'status': ''}, ... ]
>    }, ... ]

# GET /orders/order_id/
> response:
>   format: json
>   {‘deal_url’:’’, 'owner': '', ‘invitees’: [{'name': '', 'status': ''}, …], 'buy_fors': [{'name': '', 'status': ''}, ...]}
