・10mメッシュ標高のダウンロード
https://fgd.gsi.go.jp/download/menu.php

・10mメッシュ標高のインサート方法
①アプリケーションを起動
②「ファイル選択」をクリックし、標高データのXMLファイル（FG-GML-xxxx-yy-dem10b-zzzzzzzz.xml）を選択（複数ファイル選択可）
③「インサート開始」をクリックするとインサート開始


・インサートするテーブルの変更方法（プログラム内の書き換えるべき場所）

①「MainForm.cs」→「MainForm.Designer.cs」内「sqlConnection1」とコメントアウトされている中の「this.sqlConnection1.ConnectionString =」に「対象にするサーバ（Data Source）」、「対象とするDB（Initial Catalog）」を記述する

②「AltDataGetter.cs」内「InsertAltitudeData」メソッドの「bulkCopy.DestinationTableName=」に「対象とするテーブル」を記述する（mainform.Label_stateの文章も書き替えておくとわかりやすい）

③AltDataGetter.cs」内「AltitudeDataGetter」メソッドの「bulkCopy.DestinationTableName=」に「対象とするテーブル」を記述する（mainform.Label_stateの文章も書き替えておくとわかりやすい）
