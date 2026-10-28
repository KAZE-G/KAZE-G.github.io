# やままち個人網站

網站使用傳統 HTML frameset，左側導覽與播放器固定，右側內容頁切換。配色與排版刻意保留舊式個人網站的簡單外觀。

## 更新網站

- 以 GitHub Pages 發布本 repository。
- index.html 是框架入口；不要刪除 CNAME。
- model_weights.json 是既有檔案，請保留。
- 專輯資料放在 works.json；首頁更新記錄放在 updates.json。
- 不要填入不存在的音訊、歌詞或封面路徑。沒有實際檔案時，留空對應欄位。

## works.json 格式

    {
      "albums": [
        {
          "title": "專輯名稱",
          "cover": "images/cover.jpg",
          "description": "專輯簡介",
          "releaseDate": "YYYY-MM-DD",
          "format": "CD／數位發行",
          "price": "NT$ XXX",
          "details": ["製作資訊"],
          "tracks": [
            {
              "title": "曲目名稱",
              "duration": "3:00",
              "lyrics": "lyrics/track.txt",
              "audio": "audio/track.mp3"
            }
          ]
        }
      ]
    }

cover、lyrics、audio 都必須指向 repository 中實際存在的檔案。點擊曲名會在左側播放器播放該曲；上一首、下一首會在目前播放清單內循環。

## 目前內容

作品資料、價格、聯絡方式及更新記錄尚未填入；網站不會自行產生虛構曲目或聯絡資訊。
