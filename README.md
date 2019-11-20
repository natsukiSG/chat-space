## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|index: true,null: false, unique: true|
|mail|string|null: false|

### Association
・ has_many :groups, thrugh: menmbers
・ has_many :messages
・ has_manr :members