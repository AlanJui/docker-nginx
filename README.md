# 專案指引

使用 nginx 快速建立 Static Web Site 。

手邊有現成的 Static Web Site ，欲觀察其內容，可使用本專案作為「Project Template」，
透過 nginx ，快速完成 Static Web Site 的建置，以便能馬上使用瀏覽器觀察其內容。 


# 作業程序

## 建置 Docker Image 檔案作業

```bash
$ docker build -t <docker-hub-username>/nginx_site:1.0 .
```

## 執行 Docker Image 檔案作業

### (1) 啟動 Docker Container

```bash
$ docker run --rm --name web_nginx --publish 8080:80 -d <docker-hub-username>/nginx_site:1.0
```


### (2) 使用瀏覽器觀看網址： http://127.0.0.1:8080/

## 觀察 Docker Container

```bash
$ docker exec -it web-nginx bash
```

# 參考資料

 - [nginx Official Repository on Docker Hub](https://hub.docker.com/_/nginx/)