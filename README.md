# Gitbook Template 

## 為什麼做這個 ?

因為經常需要寫些有架構關聯的教學文件，加上那些教學文件很經常被散落在各地，沒什麼組織性，後來用了 GitBook 感覺被拯救了。但每次一段時間後，要重新開 GitBook 來寫新東西時，網網都忘了要裝什麼套件，以及要怎麼下相關的指令，重新學習的門檻往往也會打消你想仔細寫些東西的念頭。因此，建立這個樣板專案，省去那些常用套件安裝，直接進入內容編寫。

## 支援些什麼？

* 支援幾種常用的 gitbook plugin，請參考 `book.json` 的設定
    * Plantuml: 用來表示 UML 的圖例
    * Terminal
    * simpletabs: 在文章內用不同的 tab 切換內容
    * richquotes: 能夠用較為明顯的引言風格
    * splitter: 可以調整章節與內容間的分隔線
    * [katex](https://github.com/GitbookIO/plugin-katex): 數學式表示 
    * prismjs: 好看的原始碼風格
    * image-captions: 在圖片下方產生章節編號與圖片說明

* 可以用 GitLab CI 運行
* 支援 GitLab Pages 
* 以 Docker 作為執行環境，所建立好的 Docker Image 放在 DockerHub 中。

## 怎麼用？

先把專案複製回來: 

```
$ git clone git@github.com:vincentliao/gitbook_template.git
```


取得執行環境所需要的 Docker 映像檔:

```
$ docker pull vincentliao/gitbook_env
```

最後，就是把環境執行起來，並且編譯好樣版書，範例是把書放在 http://localhost:4000 中，開啟瀏覽器後就可以看到。

```
$ cd gitbook-template
$ docker run -it --init -p 4000:4000 -v {$PWD}:/gitbook_template gitbook-env "/gitbook-template/run.sh"
```

透過 `make serve` 執行後，會不斷的偵測書本原始內容是否有修改，倘若被改動，則會觸發重新編譯書籍，隨時可以看到修改好的內容。
