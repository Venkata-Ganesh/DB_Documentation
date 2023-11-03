# DB_Documentation

Here are the attributes of the "UserRegistration" table in a tabular format:

**UserRegistration:**

| Attribute         | Type     | Description                               |
|-------------------|----------|-------------------------------------------|
| id                | integer  | Unique identifier for user registration (Primary Key) |
| email             | varchar  | User's email address for registration     |
| contact_number    | varchar  | User's contact number for registration    |
| password_hash     | varchar  | Hashed password for user registration     |

The "UserRegistration" table typically stores information related to user registration, including the user's email address, contact number, and a hashed password for authentication.

**User**

Here are the attributes of the "User" table in a tabular format:

| Attribute               | Type        | Description                                           |
|-------------------------|-------------|-------------------------------------------------------|
| id                      | integer     | Unique identifier for the user (Primary Key)          |
| username                | varchar     | User's username                                       |
| full_name               | varchar     | User's full name                                      |
| email                   | varchar     | User's email address                                 |
| password_hash           | varchar     | Hashed password for user authentication               |
| dob_month               | integer     | Month of the user's date of birth                    |
| dob_day                 | integer     | Day of the user's date of birth                      |
| is_public               | boolean     | Indicates if the user's profile is public (true/false)|
| contact_number          | varchar     | User's contact number                                |
| city                    | varchar     | User's city of residence                             |
| country                 | varchar     | User's country of residence                          |
| address                 | varchar     | User's postal address                                |
| preferred_language      | varchar[]   | Array of preferred languages                         |
| primary_language        | varchar     | User's primary language                              |
| profile_image_url       | varchar     | URL for the user's profile image                     |
| cover_image_url         | varchar     | URL for the user's cover image                       |
| is_active               | boolean     | Indicates if the user's account is active (true/false)|
| bio                     | varchar     | User's biography or description                      |
| created_at              | datetime    | Date and time of user account creation               |
| updated_at              | datetime    | Date and time of user account update                 |
| device_os               | varchar     | User's device operating system                       |
| last_login              | timestamp   | Date and time of the user's last login               |
| website_urls            | varchar(500)[] | Array of website URLs associated with the user     |
| privacy_settings        | jsonb       | JSON data for privacy settings                       |
| notification_settings   | jsonb       | JSON data for notification settings                   |
| user_role               | varchar     | User's role or access level                           |
| verification_status     | boolean     | Verification status of the user's account (true/false)|
| ip_address              | varchar     | User's IP address                                    |
| last_password_change    | timestamp   | Date and time of the user's last password change     |
| last_seen               | varchar     | User's last seen status or timestamp                  |

Please note that this is a comprehensive list of attributes for a user in the database, and some attributes might not be present or applicable to all users.


Here are the attributes of the "Content" table in a tabular format:

| Attribute               | Type        | Description                                           |
|-------------------------|-------------|-------------------------------------------------------|
| id                      | integer     | Unique identifier for the content (Primary Key)       |
| aws_url                 | varchar     | URL or path to the content stored on AWS              |
| type                    | enum        | Type of content (e.g., video, article, etc.)           |
| description             | text        | A detailed description of the content                  |
| title                   | varchar     | Title or name of the content                           |
| likes                   | integer     | Number of likes or upvotes for the content             |
| dislikes                | integer     | Number of dislikes or downvotes for the content        |
| share_url               | varchar     | URL for sharing the content                            |
| category                | varchar     | Category or topic of the content                       |
| ratings                 | decimal     | Average ratings or user reviews for the content        |
| skill_set               | text        | Skills that can be gained from the content             |
| certificate_template    | text        | Template for the course completion certificate        |
| thumbnail               | varchar     | URL or path to the content's thumbnail or image        |
| feedback                | text        | User feedback or comments on the content               |
| views                   | integer     | Number of views or times the content has been viewed   |
| share_count             | integer     | Number of times the content has been shared            |
| user_id                 | integer     | User ID (Foreign Key) of the content's creator          |

The "skill_set" attribute represents the skills that users can acquire from the content, and "certificate_template" is the template for the course completion certificate associated with the content.


Certainly, here are the attributes of the listed tables in a tabular format:

**Playlist:**

| Attribute           | Type       | Description                                     |
|---------------------|------------|-------------------------------------------------|
| id                  | integer    | Unique identifier for the playlist (Primary Key)|
| title               | varchar    | Title of the playlist                           |
| description         | varchar    | Description or details about the playlist       |
| thumbnail           | varchar    | URL or path to the playlist's thumbnail image    |
| date_created        | datetime   | Date and time when the playlist was created     |
| privacy_setting     | enum       | Privacy setting for the playlist                |
| tags                | varchar    | Tags or labels associated with the playlist     |
| video_count         | integer    | Number of videos in the playlist                |
| likes               | integer    | Number of likes for the playlist                |
| dislikes            | integer    | Number of dislikes for the playlist             |
| duration_minutes    | integer    | Total duration of the playlist in minutes       |
| favorite_count      | integer    | Number of times the playlist has been favorited |
| view_count          | integer    | Number of times the playlist has been viewed    |
| user_id             | integer    | User ID (Foreign Key) of the playlist's creator |

**Subscription:**

| Attribute             | Type     | Description                                      |
|-----------------------|----------|--------------------------------------------------|
| id                    | integer  | Unique identifier for the subscription (Primary Key) |
| plan/type             | enum     | Type of subscription plan                        |
| amount                | double   | Subscription amount (price)                     |
| start_date            | datetime | Date and time when the subscription started     |
| end_date              | datetime | Date and time when the subscription ends        |
| status                | enum     | Status of the subscription (e.g., active, canceled) |
| payment_method        | varchar  | Payment method used for the subscription        |
| renewal_date          | datetime | Date and time for subscription renewal          |
| cancellation_date     | datetime | Date and time when the subscription was canceled |
| subscription_features | varchar  | Features included in the subscription            |
| billing_address       | text     | Billing address information                      |
| transaction_id        | integer  | Identifier for the subscription transaction      |
| coupon_code           | varchar  | Coupon code used for the subscription            |
| trial_period          | integer  | Duration of the trial period, if applicable     |
| subscription_history  | text     | Subscription history and details                 |
| refund_information    | text     | Information about refunds, if applicable        |
| user_id               | integer  | User ID (Foreign Key) associated with the subscription |

**User_Tokens:**

| Attribute           | Type       | Description                                |
|---------------------|------------|--------------------------------------------|
| id                  | integer    | Unique identifier for user tokens (Primary Key) |
| token               | varchar    | Token for user authentication or authorization |
| signature           | varchar    | Signature for token verification            |
| expiration_time     | datetime   | Date and time when the token expires        |
| last_logout_time    | datetime   | Date and time of the user's last logout     |
| user_id             | integer    | User ID (Foreign Key) associated with the token |

**Activity:**

| Attribute           | Type       | Description                                     |
|---------------------|------------|-------------------------------------------------|
| id                  | integer    | Identifier for the activity                      |
| activity_type       | enum       | Type of activity (e.g., like, comment, etc.)    |
| content_id          | integer    | Identifier for the related content              |
| created_at          | timestamp  | Date and time when the activity was created     |
| user_id             | integer    | User ID (Foreign Key) associated with the activity |

Thank you for the additional information. In the "Connection" table, where "connection_type" can be 1st, 2nd, or 3rd, you can represent it as follows:

**Connection:**

| Attribute           | Type       | Description                                    |
|---------------------|------------|------------------------------------------------|
| id                  | integer    | Unique identifier for the connection (Primary Key) |
| user_id1            | integer    | User ID of the first user in the connection    |
| user_id2            | integer    | User ID of the second user in the connection   |
| connection_type     | varchar    | Type of connection (e.g., 1st, 2nd, 3rd)     |
| created_at          | timestamp  | Date and time when the connection was created  |

You can use the "connection_type" values as 1st, 2nd, or 3rd to represent different levels or types of connections between users.

**Message:**

| Attribute           | Type       | Description                              |
|---------------------|------------|------------------------------------------|
| sender_user_id     | integer    | User ID of the message sender           |
| receiver_user_id   | integer    | User ID of the message receiver         |
| message            | varchar    | The content of the message              |
| file_url           | varchar    | URL or path to an attached file (if any) |

**Review:**

| Attribute           | Type       | Description                                     |
|---------------------|------------|-------------------------------------------------|
| id                  | integer    | Unique identifier for the review (Primary Key)  |
| review_text         | text       | Text of the review                               |
| user_id             | integer    | User ID (Foreign Key) of the review's author    |
| content_id          | integer    | Identifier for the content being reviewed      |

These tables store various information related to users, content, subscriptions, activities, connections, messages, and reviews.


Certainly, here are the attributes of the additional tables you've provided in a tabular format:

**Transaction:**

| Attribute   | Type     | Description                                        |
|-------------|----------|----------------------------------------------------|
| id          | integer  | Unique identifier for the transaction (Primary Key)|
| time_stamp  | datetime | Date and time of the transaction                    |
| amount      | double   | Transaction amount                                 |
| trans_type  | enum     | Type of transaction (e.g., purchase, refund, etc.) |
| status      | enum     | Status of the transaction (e.g., completed, pending) |
| product     | integer  | Foreign Key referencing the related product        |
| from        | integer  | Foreign Key referencing the sender or source       |
| user_id     | integer  | Foreign Key referencing the user associated with the transaction |

**Address:**

| Attribute       | Type     | Description                                     |
|-----------------|----------|-------------------------------------------------|
| id              | integer  | Unique identifier for the address (Primary Key) |
| house/flat no   | varchar  | House or flat number                            |
| street          | varchar  | Street or address                               |
| city            | varchar  | City or locality                                |
| pin/zip_code    | integer  | Postal or zip code                              |
| state           | varchar  | State or region                                 |
| country         | varchar  | Country                                         |
| user_id         | integer  | Foreign Key referencing the user associated with the address |

**Notification:**

| Attribute        | Type     | Description                                |
|------------------|----------|--------------------------------------------|
| id               | integer  | Unique identifier for the notification (Primary Key) |
| message          | varchar  | Content of the notification                 |
| type             | enum     | Type of notification (short or Long duration lifetime) |
| expiration_time  | datetime | Date and time when the notification expires |
| created_at       | datetime | Date and time when the notification was created |
| user_id          | integer  | Foreign Key referencing the user associated with the notification |

**Vote:**

| Attribute      | Type     | Description                                   |
|----------------|----------|-----------------------------------------------|
| id             | integer  | Unique identifier for the vote (Primary Key) |
| type_id        | integer  | Identifier for the vote type                  |
| content_id     | integer  | Foreign Key referencing the content being voted on |
| user_id        | integer  | Foreign Key referencing the user who cast the vote |

**Forum:**

| Attribute     | Type     | Description                                |
|---------------|----------|--------------------------------------------|
| id            | integer  | Unique identifier for the forum (Primary Key) |
| title         | varchar  | Title of the forum                          |
| description   | varchar  | Description or details about the forum     |
| categories    | enum     | Categories or topics of the forum          |
| tags          | varchar  | Tags or labels associated with the forum   |
| content_id    | integer  | Foreign Key referencing the related content |
| user_id       | integer  | Foreign Key referencing the user who created the forum |

Please note that the specific values of "enum" fields can vary based on your application's needs.


Certainly, here are the attributes for the remaining tables you provided:

**UsertoPollMapper:**

| Attribute        | Type     | Description                                   |
|------------------|----------|-----------------------------------------------|
| poll_id          | integer  | Identifier for the associated poll            |
| user_id          | integer  | Identifier for the user (Foreign Key)         |
| user_response    | integer[] | Array of user responses to the poll           |

**CollegetoContentMapper:**

| Attribute        | Type     | Description                                   |
|------------------|----------|-----------------------------------------------|
| id               | integer  | Unique identifier for the mapper (Primary Key) |
| content_id       | integer  | Identifier for the associated content         |
| college_id       | integer  | Identifier for the associated college         |

**UsertoContentMapper:**

| Attribute        | Type     | Description                                   |
|------------------|----------|-----------------------------------------------|
| id               | integer  | Unique identifier for the mapper (Primary Key) |
| content_id       | integer  | Identifier for the associated content         |
| user_id          | integer  | Identifier for the user (Foreign Key)         |

These tables represent mappings or associations between users, polls, content, colleges, and their respective attributes.

Certainly, here are the attributes for the "ChanneltoGroupMapper" table:

**ChanneltoGroupMapper:**

| Attribute            | Type     | Description                                       |
|----------------------|----------|---------------------------------------------------|
| parent_group_id      | integer  | Identifier for the parent group                   |
| child_group_id       | integer  | Identifier for the child group                    |

This table represents the mapping or association between parent and child groups, possibly indicating relationships between channels and groups.
