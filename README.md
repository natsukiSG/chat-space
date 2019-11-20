チャットスペース（chat-space）

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|reference|null: false, foreign_key: true|
|group_id|reference|null: false, foreign_key: true|

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|reference|null: false, foreign_key: true|
|name|string|null: false|

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|group_id|reference|null: false, foreign_key: true|
|name|string|null: false|

## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|body|text|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|
|image|integer|null: false|
|group_id|integer|null: false|

### Association
- belongs_to :group
- belongs_to :user
- belongs_to :body
- has_many : group, users
