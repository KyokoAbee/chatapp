# ①課題番号-プロダクト名
小学校低学年向け しりとりアプリ!!


## ②課題内容（どんな作品か）
しりとりをしながら、英単語を学べるアプリです


## ③工夫した点・こだわった点
- Firestore に保存されたテキストのうち、タイムスタンプが一番新しいデータだけが表示されます
- 「ん」で終わる言葉、しりとりになっていない言葉を入力するとアラートが出ます
- 「ちゃ」「のばし棒」なども正規化してから、文字比較を行うようにしています
- Azure AI Translator API と連携し単語を翻訳し、表示しています
- 翻訳した単語は、紐づくドキュメントID に保存されます


## ④難しかった点・次回トライしたいこと(又は機能)
- Firestore に保存されているすべてのデータを履歴として表示したかったです。
- OpenAI API、Gemini API との連携を試みましたが、CORS(Cross-Origin-Resource-Sharing)のエラーが解消できず断念…
- 今回もcss にあまり時間をかけられませんでした…次こそは。。


## ⑤質問・疑問・感想、シェアしたいこと等なんでも
- onSnapshotを使うと、入力時と保存時に自動で2回文字比較が行われてしまい、しりとりにならないので、getDoc でFirestore 上のデータを引っ張ってきました。
  データを取得するにしても、複数の方法があるのだと学びました。
- 他のサービスと連携させたい！となったときにAPI という仕組みはとても便利だなーと感じました。