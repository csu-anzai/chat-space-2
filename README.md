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
|name|string|null: false, foreign_key: true|


### Association
- has_many :messages
- belongs_to :group
- belongs_to :groups_user


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|


### Association
has_many :users
belongs_to :groups_user



## messagesテーブル
|Column|Type|Options|
|------|----|-------|

|text|text|null: false|
|image|string|null: false|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|


## Association
- belongs_to :group
- belongs_to :user

