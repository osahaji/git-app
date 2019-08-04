## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|username|string|null: false|
### Association
- belongs_to :group
- belogns_to :chat
-has_many :users, through: :groups


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false, foreign_key: true|
|group_name|integer|null: false, foreign_key: true|
|group_members|integer|null: false, foreign_key: true|
### Association
- has_many:users through :members
- has_many:members

##messagesテーブル
|Column|Type|Options|
|------|----|-------|
|body|text|null: false|
|image|string|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|created_at|
### Association
- belongs_to :user
- has_many :groups

##membersテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
-belongs_to :group
-has_many: users


