# Netdata Docker 監控環境

本專案透過 Docker 快速建構 Netdata 監控服務，適用於自架伺服器的即時系統監控。

## 特色

- 以 Netdata 官方映像檔建構
- 支援持久化設定與資料
- 監控主機多項系統資訊
- 免安裝額外相依套件

## 快速開始

1. 複製範本設定檔：

   ```sh
   cp docker-compose.yml.dist docker-compose.yml
   ```

2. 啟動 Netdata 服務：

   ```sh
   docker compose up -d
   ```

3. 於瀏覽器開啟 `http://localhost:19999` 進行監控。

## 目錄結構

- `docker-compose.yml.dist`：Netdata Docker Compose 原理圖範本
- `README.md`：本文件

## 主要設定說明

- 監控服務預設監聽 19999 埠口
- 重要資料與設定皆以 volume 持久化
- 需掛載主機 `/proc`、`/sys` 等目錄以取得完整監控資訊

## 停止與移除

```sh
docker compose down
```

## 參考資訊

- [Netdata 官方文件](https://learn.netdata.cloud/docs/agent/packaging/docker/)
- [Netdata GitHub](https://github.com/netdata/netdata)

---

如需進階設定，請參考 Netdata 官方指南。