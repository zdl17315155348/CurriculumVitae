# Personal Resume Editor (简历编辑器)

这是一个基于 Vue.js (前端) 和 Django (后端) 的个人简历编辑器项目。支持所见即所得的简历编辑、模块拖拽排序、自定义配置以及 PDF 导出功能。

## 🚀 快速启动

1. 确保已安装 Python 和 Django。
2. 打开终端。
3. 运行以下命令：

```bash
python manage.py runserver
```

4. 在浏览器中访问：[http://127.0.0.1:8000/](http://127.0.0.1:8000/)

## 📂 项目结构

- **dist/**: 前端构建输出目录。
- **templates/**: Django 模板目录（`index.html` 的源文件，已适配 Vue 语法）。
- **static/**: 静态资源目录。
- **core/**: Django 应用核心逻辑。
- **config/**: Django 项目配置。
- **manage.py**: Django 项目管理脚本。

## ✨ 主要功能

- **所见即所得编辑**：左侧编辑，右侧实时预览。
- **模块管理**：
  - 支持模块显示/隐藏。
  - 支持模块拖拽排序。
  - 支持自定义模块名称。
- **Markdown 支持**：专业技能和工作经历支持 Markdown 语法渲染。
- **PDF 导出**：一键生成 A4 格式的 PDF 简历。
- **本地存储**：自动保存编辑进度到本地浏览器。
