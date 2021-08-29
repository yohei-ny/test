# デバック内容
## 1.投稿できない
- post 'todolists' => 'todolists#create'
 > 上記の記述がconfigにない

## 2.indexで削除できない
- method: :delete
 > 上記の記述がlinkに含まれていない

## 3.indexで一覧画面が出ない
- 変数が違うため→@listが@listになっている