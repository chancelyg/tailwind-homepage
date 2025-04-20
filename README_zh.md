# 个人导航主页

一个基于HTML、TailwindCSS和YAML配置构建的简洁优雅个人导航页面。

## 项目结构

项目仅有 2 个文件，如下：

```
.
├── config.yaml        # 站点配置文件（分类和链接）
├── index.html         # 主应用页面
```

## 功能特性

项目功能特性如下：
- 采用TailwindCSS实现的清爽响应式设计
- 通过YAML文件可配置分类和链接
- 实时搜索功能
- 悬停效果和现代化UI界面

## 部署运行

搭配 nginx 配置访问 `index.html` 文档

部署步骤：
1. 克隆仓库
2. 复制配置文件 `cp .config.yaml config.yaml` 
3. 根据个人需要自行修 `config.yaml` 内容


nginx 配置参考如下：

```conf
server {
    listen 80;  # 监听 80 端口
    server_name your_domain.com;  # 将 your_domain.com 替换为你的域名或 IP 地址

    root /path/tailwind-homepage;  # 指定根目录
    index index.html;  # 指定默认的索引文件

    location / {
        try_files $uri $uri/ =404;  # 尝试访问请求的 URI，如果不存在则返回 404
    }

    # 可以添加错误页面配置（可选）
    error_page 404 /404.html;  # 404 错误页面
    location = /404.html {
        internal;  # 只允许内部请求
    }
}
```

## 开发技术

本项目使用：
- TailwindCSS（通过CDN引入）
- js-yaml用于YAML解析
- Python内置HTTP服务器用于开发

如果需要调试，可以使用 vscode 进行配置调试，`.launch.json` 文件如下：

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Python: HTTP Server",
            "type": "debugpy",
            "request": "launch",
            "module": "http.server",
            "args": [
                "8000"
            ],
            "console": "internalConsole"
        }
    ]
}
```