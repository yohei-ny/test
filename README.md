# デバック内容


## 1.indexで表示されない
- 1行目クラスの名前がおかしい
 > TdolistsController→TodolistsControllerにする

## 2.アタッチメントでエラーが吐く
- app/models/list.rbにattachmentのimageに_idがある
 > app/models/list.rbにattachmentのimage_idの_idを消す

## 3.createアクションに遷移ができない
- config/routes.rbにcreateアクションがない
 > post 'todolists' => 'todolists#create'を追加

## 4.新規投稿ができない
- Strong paramaterのrequireがない、imageに_idが付与されている
 > params.require(:list).permit(:title, :body, :image)とすれば良い

## 5.indexで削除できない
- method: :delete
 > method: :deleteをlinkに付与する

