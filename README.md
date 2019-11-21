チャットスペース（chat-space）

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|reference|null: false, foreign_key: true|
|group_id|reference|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user
------------------------------
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|username|string|null: false|
### Association
- has_many :tweets
- has_many :messages
------------------------------
## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|group|reference|null: false, foreign_key: true|
|user|reference|null: false, foreign_key: true|
|id|integrer|null: false|

### Association
has_many: users
------------------------------
## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|
|image|integer|null: false|
|group_id|integer|null: false|

### Association
- belongs_to :user
------------------------------