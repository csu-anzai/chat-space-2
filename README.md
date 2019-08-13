# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|integer|null: false, foreign_key: true|
|password|||
|email|


### Association
belongs_to :groups
belongs_to :groups_users

|password|string|null: false, foreign_key: true|
|email|string|null: false, foreign_key: true|


### Association
- has_many :messages
- belongs_to :groups
- belongs_to :groups_users


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|group_name|integer|null: false, foreign_key: true|


### Association
belongs_to :users
belongs_to :groups_users

|group_name|string|null: false, foreign_key: true|

### Association
- belongs_to :users
- belongs_to :groups_users


## messagesテーブル
|Column|Type|Options|
|------|----|-------|

|text|integer|null: false, foreign_key: true|
|image|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|


|text|text|null: false, foreign_key: true|
|image|text|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

## Association
- belongs_to :groups
- belongs_to :users

