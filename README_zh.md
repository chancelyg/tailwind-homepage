# 个人导航主页

一个基于HTML、TailwindCSS和YAML配置构建的简洁优雅个人导航页面。

## 项目结构

```
.
├── config.yaml        # 站点配置文件（分类和链接）
├── index.html         # 主应用页面
├── .vscode/          # VS Code配置目录
└── README.md         # 项目文档
```

## 功能特性

- 采用TailwindCSS实现的清爽响应式设计
- 通过YAML文件可配置分类和链接
- 实时搜索功能
- 悬停效果和现代化UI界面

## 安装与运行

1. 克隆本仓库
2. 确保已安装Python（推荐Python 3.x）
3. 运行开发服务器：
   ```bash
   python -m http.server
   ```
4. 在浏览器访问 `http://localhost:8000`

## 配置说明

编辑`config.yaml`自定义导航链接：

```yaml
categories:
  - name: 分类名称
    color: indigo-600
    sites:
      - name: 网站名称
        url: https://example.com
        icon: EX
        iconBg: bg-blue-500
        iconColor: text-white
```

## 开发技术

本项目使用：
- TailwindCSS（通过CDN引入）
- js-yaml用于YAML解析
- Python内置HTTP服务器用于开发

包含VS Code启动配置便于调试。