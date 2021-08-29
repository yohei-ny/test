# デバック内容
## 1.投稿できない
- post 'todolists' => 'todolists#create'
 > 上記の記述がconfigにない

## 2.indexで削除できない
- method: :delete
 > 上記の記述がlinkに含まれていない

## 3.indexで一覧画面が出ない
- 変数が違うため→@listが@listになっている


## 4. app/controller/todolists_controller
- 1行目クラスの名前を変更
- Strong paramaterのrequireを削除、imageに_idを追加

## 5.app/models/list.rb
- attachmentのimageに_idを
