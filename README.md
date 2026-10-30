# 星穹放置 · Star Realm Idle

单文件网页放置游戏，零依赖，纯前端，无需构建、无需后端。

## 快速部署

把 `index.html` 上传到任意静态托管即可。

### 方式一：Nginx

```nginx
server {
    listen 80;
    server_name your-domain.com;
    root /var/www/star-realm;
    index index.html;
    location / {
        try_files $uri $uri/ =404;
    }
}
```

上传后 `nginx -s reload` 即可。

### 方式二：任意静态服务器

```bash
# Python 快速起一个本地/服务器服务
python3 -m http.server 8080
# 访问 http://服务器IP:8080
```

### 方式三：GitHub Pages / Vercel / Netlify / 对象存储

直接把 `index.html` 推上去即可，均支持纯静态托管。

## 存档说明

- **自动保存**：进度存于浏览器 localStorage，每 15 秒 + 关闭页面时自动保存，刷新/重开不丢档。
- 存档按「域名」隔离，换域名、换浏览器或清除浏览器数据会丢档。
- **云存档（可选）**：游戏内「云存档」页 → 生成仅 `gist` 权限的 GitHub Token → 连接后一键上传/下载，可跨设备同步。

## 目录结构

```
star-realm-idle/
├── index.html    # 游戏本体（唯一必需文件）
└── README.md     # 本说明
```
