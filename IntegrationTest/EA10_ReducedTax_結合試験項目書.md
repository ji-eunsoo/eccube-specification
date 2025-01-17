# EA10_ReducedTax_結合試験項目書

<!-- UC01：基本設定 -->

## EA1001-UC01-T01_基本税率設定

1. 設定 → 店舗設定 → 税率設定
1. 税率「10%」、課税規則を「切り捨て」、適用日時「現日時」で設定する
1. ”新規作成”ボタンを押下する
1. 完了メッセージが表示される
1. フロントの商品詳細画面で商品の価格を確認し、税率が正しく設定されていることを確認する

## EA1001-UC01-T02_個別税率設定

1. 設定 → 店舗設定 → 基本設定
1. 税設定を有効にする
1. ”登録”ボタンを押下する
1. 完了メッセージが表示される
1. 商品管理 → 商品登録
1. 税率の設定フォームが表示されていることを確認する

<!-- UC02：商品管理 -->

## EA1001-UC02-T01_商品登録

1. 事前準備として「EA1001-UC01-T02」の税設定を有効に設定しておく
1. 商品管理 → 商品登録
1. 商品登録フォームに必須な情報を入力する
1. 公開ステータスを「公開」に設定する
1. ”登録”ボタンを押下する
1. 完了メッセージが表示される
1. ”商品を確認”ボタンを押下する
1. 商品の確認画面で税額が正しく表示されていることを確認する

## EA1001-UC02-T02_商品登録（個別税率有り）

1. 商品管理 → 商品登録
1. 商品登録フォームに必須な情報を入力する
1. 税率に「8」%を設定する
1. 公開ステータスを「公開」に設定する
1. ”登録”ボタンを押下する
1. 完了メッセージが表示される
1. ”商品を確認”ボタンを押下する
1. 商品の確認画面で税額が正しく表示されていることを確認する

## EA1001-UC02-T03_商品登録（個別税率有り/規格有り）

1. 商品管理 → 商品登録
1. 商品登録フォームに必須な情報を入力する
1. 税率に「8」%を設定する
1. 公開ステータスを「公開」に設定する
1. ”登録”ボタンを押下する
1. 完了メッセージが表示される
1. 商品規格情報が表示されていることを確認する
1. "この商品の規格を確認"ボタンを押下する
1. 確認モーダルで、"保存して移動"ボタンを押下する
1. 商品規格登録画面で、「規格1」「規格2」を設定する
1. ”商品規格の設定”ボタンを押下する
1. 商品規格の登録フォームに必須な情報を入力する
1. 税率に「8」%を設定する
1. ”登録”ボタンを押下する
1. 完了メッセージが表示される
1. フロント画面で設定した商品の詳細情報を表示し、税額が正しく表示されていることを確認する

## EA1001-UC02-T04_商品CSVのダウンロード

1. 商品管理 → 商品一覧
1. ”CSV出力項目設定”ボタンを押下する
1. CSV出力項目設定で「税率」を出力する項目に追加する
1. ”登録”ボタンを押下する
1. 完了メッセージが表示される
1. 商品管理 → 商品一覧
1. ”CSVダウンロード”ボタンを押下する
1. CSVファイルがダウンロードされる
1. CSVファイルに「税率」のカラムが設定され、商品ごとに「税率」が正しく設定されていることを確認する

## EA1001-UC02-T05_商品CSV登録

1. 商品管理 → 商品CSV登録
1. "雛形ファイルダウンロード"ボタンを押下する
1. CSVファイルがダウンロードされる
1. CSVファイルの２行目に、「公開ステータス(ID)」を1、「商品名」を任意、「販売種別(ID)」を1、「在庫数無制限フラグ」を1、「販売価格」を数値、「税率」「8」%で設定し保存する
1. 商品CSV登録画面の「CSVファイルを選択」のフォームから、保存したCSVファイルを選択する
1. "一括登録を実行"ボタンを押下する
1. 完了メッセージが表示される
1. フロント画面で設定した商品の詳細情報を表示し、税額が正しく表示されていることを確認する

## EA1001-UC02-T06_商品CSV登録

1. 事前準備として、「EA1001-UC02-T03」で登録した商品を使用する
1. 商品管理 → 商品CSV登録
1. 「EA1001-UC02-T03」で使用したCSVファイルの２行目の、「商品ID」を登録されたIDで設定、「税率」「10」%で設定し保存する
1. 商品CSV登録画面の「CSVファイルを選択」のフォームから、保存したCSVファイルを選択する
1. "一括登録を実行"ボタンを押下する
1. 完了メッセージが表示される
1. フロント画面で設定した商品の詳細情報を表示し、税額が正しく表示されていることを確認する

<!-- UC03：受注管理 -->

## EA1001-UC03-T01_受注登録

1. 事前準備として、「EA1001-UC02-T01」「EA1001-UC02-T02」「EA1001-UC02-T03」で登録した商品を購入可能な状態としておく
1. 受注管理 → 受注登録
1. 受注登録フォームに必須な情報を入力する
1. 「EA1001-UC02-T01」「EA1001-UC02-T02」「EA1001-UC02-T03」登録された商品を、商品情報の”商品追加”ボタンから登録する
1. "登録"ボタンを押下する
1. 完了メッセージが表示される
1. 商品情報に含まれている商品の税率ごとの金額が表示され、お支払い合計や加算ポイントが正しく計算されていることを確認(加算ポイントについては設定のポイント設定の値を確認しておき、受注情報を確認する)

## EA1001-UC03-T02_受注登録（複数配送）

1. 事前準備として、「EA1001-UC02-T01」「EA1001-UC02-T02」「EA1001-UC02-T03」で登録した商品を購入可能な状態としておく
1. 受注管理 → 受注登録
1. 受注登録フォームに必須な情報を入力する
1. 「EA1001-UC02-T01」「EA1001-UC02-T02」「EA1001-UC02-T03」登録された商品を、商品情報の”商品追加”ボタンから登録する
1. "登録"ボタンを押下する
1. 完了メッセージが表示される
1. 出荷情報から”出荷情報の追加”ボタンを押下する
1. 確認モーダルで”保存して移動”ボタンを押下する
1. 出荷登録画面で”出荷情報の追加”ボタンを押下し、”出荷情報(2)”のフォームが表示されることを確認する
1. ”出荷情報(2)”のフォームに必須な情報を入力する
1. 「EA1001-UC02-T01」「EA1001-UC02-T02」「EA1001-UC02-T03」登録された商品を、”出荷情報(2)”のフォームの”商品を追加”ボタンから登録する
1. "登録"ボタンを押下する
1. 完了メッセージが表示される
1. 受注登録画面にもどる
1. 商品情報に含まれている商品の税率ごとの金額が表示され、お支払い合計や加算ポイントが正しく計算されていることを確認する

## EA1001-UC03-T03_受注明細の変更による再計算

- 受注登録
1. 事前準備として、「EA1001-UC02-T01」「EA1001-UC02-T02」「EA1001-UC02-T03」で登録した商品を購入可能な状態としておく
1. 受注管理 → 受注登録
1. 受注登録フォームに必須な情報を入力する
1. 「EA1001-UC02-T01」「EA1001-UC02-T02」「EA1001-UC02-T03」登録された商品を、商品情報の”商品追加”ボタンから登録する
1. "登録"ボタンを押下する
1. 完了メッセージが表示される
1. 商品情報に含まれている商品の税率ごとの金額が表示され、お支払い合計や加算ポイントが正しく計算されていることを確認する

- 商品数量の変更

1. 商品情報から商品の数量を変更し、”計算結果を更新”ボタンを押下する
1. 商品情報に含まれている商品の税率ごとの金額が表示され、お支払い合計や加算ポイントが正しく計算されていることを確認する

- その他明細の追加

1. 商品情報から”その他明細の追加”ボタンを押下する
1. 設定用のモーダルから項目の”+”ボタンで追加する
1. 追加した項目に金額と税率を設定し、”計算結果を更新”ボタンを押下する
1. 商品情報に含まれている商品の税率ごとの金額が表示され、お支払い合計や加算ポイントが正しく計算されていることを確認する

- ポイントの利用

1. 利用ポイントのフォームにポイントを設定する
1. "登録"ボタンを押下する
1. 完了メッセージが表示される
1. 商品情報に含まれている商品の税率ごとの金額が表示され、お支払い合計や加算ポイントが正しく計算されていることを確認する

- 商品情報の変更

1. 商品管理 → 商品一覧
1. 商品情報に含まれている商品の中で個別税率が設定されている商品の税率設定を変更する
1. 受注登録画面に戻り、”計算結果を更新”ボタンを押下する
1. 商品情報に含まれている商品の税率ごとの金額が変更されず、お支払い合計や加算ポイントなど設定が有効な際と変わらない金額が表示されていることを確認する
1. "登録"ボタンを押下する
1. 完了メッセージが表示される
1. 商品情報に含まれている商品の税率ごとの金額が変更されず、お支払い合計や加算ポイントなど設定が有効な際と変わらない金額が表示されていることを確認する

- 個別税率設定の無効化

1. 設定 → 店舗設定 → 基本設定
1. 税設定を無効にする
1. ”登録”ボタンを押下する
1. 完了メッセージが表示される
1. 受注登録画面に戻り、”計算結果を更新”ボタンを押下する
1. 商品情報に含まれている商品の税率ごとの金額が変更されず、お支払い合計や加算ポイントなど設定が有効な際と変わらない金額が表示されていることを確認する
1. "登録"ボタンを押下する
1. 完了メッセージが表示される
1. 商品情報に含まれている商品の税率ごとの金額が変更されず、お支払い合計や加算ポイントなど設定が有効な際と変わらない金額が表示されていることを確認する