チャットスペース（chat-space）

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

## bodyテーブル
|Column|Type|Options|
|------|----|-------|
|image|string|index: true,null: false, unique: true|
|name|string|index: true,null: false, unique: true|
|mail|string|null: false|

## commentテーブル
|Column|Type|Options|
|------|----|-------|
|comment|text|index: true,null: false, unique: true|
|name|string|index: true,null: false, unique: true|
|mail|string|null: false|

## imageテーブル
|Column|Type|Options|
|------|----|-------|
|image|string|index: true,null: false, unique: true|
|name|string|index: true,null: false, unique: true|
|mail|string|null: false|

### Association
- belongs_to :group
- belongs_to :user
- has_many image, comment
 

