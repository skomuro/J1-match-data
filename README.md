# J1 Match Data

このリポジトリは、2014～2025のJ1リーグの試合データをまとめたデータ置き場です。  
データは [Football LAB](https://www.football-lab.jp/) からスクレイピングで取得しました。


## データ構造

- `YYYY/` ディレクトリ  
  各シーズンごとにフォルダを作成  
  - 例: `2025/`

- `(teamname)_match_stats.csv`  
  チームごとの試合データを格納  
  - `teamname` は teamname は Football LAB の チームコード（URLスラッグ） に従います。  
    - 例: `y-fm_match_stats.csv`


## データ内容

CSV ファイルには各試合のスタッツが行単位で格納されています。  

### 主な列

- `HOME/AWAY` … ホーム or アウェイ  
- `Opponent` … 対戦相手  
- `勝敗` … 勝ち(W)/引き分け(D)/負け(L)  
- `(teamname)_得点`, `(teamname)_失点` … 得点・失点  
- `Opponent_ゴール期待値`, `(teamname)_ゴール期待値` … xG (ゴール期待値)  
- `Opponent_シュート`, `(teamname)_シュート` … シュート数  
- `Opponent_パス`, `(team)_パス` … パス数  
- `Opponent_総移動距離`, `(teamname)_総移動距離` … 総走行距離  
- `Opponent_スプリント`, `(teamname)_スプリント` … スプリント回数  
- `Opponent_ボール保持率`, `(teamname)_ボール保持率` … ボール支配率  
- `URL` … 出典試合ページへのリンク  

その他、クロス、ドリブル、クリア、警告・退場、30mライン進入、PA進入、チャンス構築率 など多様なスタッツが含まれます。  
列名は `Opponent_` と `(teamname)_` に分かれており、**相手チーム vs 自チーム** の値を表しています。
