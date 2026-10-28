# やままち個人網站

網站使用傳統 HTML frameset，左側導覽與播放器固定，右側內容頁切換。配色與排版刻意保留舊式個人網站的簡單外觀。

## 更新網站

- 以 GitHub Pages 發布本 repository。
- index.html 是框架入口；不要刪除 CNAME。
- model_weights.json 是既有檔案，請保留。
- 專輯資料放在 works.json；首頁更新記錄放在 updates.json。
- 音樂檔和封面放在 WORKS/<專輯資料夾>/；歌詞使用實際存在的文字檔。
- 不要填入不存在的音訊、歌詞或封面路徑。
- 更換既有素材後若瀏覽器仍載入舊版本，更新 site-config.json 的 assetVersion。

## 全站音樂資料夾

site-config.json 設定共用路徑和素材版本：

    {
      "worksDir": "/WORKS/",
      "assetVersion": "20261028-1"
    }

## works.json 格式

每張專輯只設定一次 dir；封面和曲目可以只寫檔名：

    {
      "albums": [
        {
          "title": "專輯名稱",
          "dir": "EP01",
          "cover": "cover.jpg",
          "tracks": [
            {
              "title": "曲目名稱",
              "duration": "3:00",
              "file": "track.mp3",
              "lyrics": "lyrics/track.txt"
            }
          ]
        }
      ]
    }

相對檔名會接在全站 worksDir 和專輯 dir 後面；也可以在 cover、file 或 lyrics 填完整網站路徑。每個路徑都必須對應到 repository 中實際存在的檔案。點擊曲名會在左側播放器播放該曲；上一首、下一首會在目前播放清單內循環。
