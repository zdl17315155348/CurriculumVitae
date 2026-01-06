# Personal Resume Editor (简历编辑器)

这是一个基于 Vue.js (前端) 和 Django (后端) 的现代化个人简历生成器。支持所见即所得的编辑体验、高度自定义的模块管理、响应式布局以及高质量的 PDF 导出功能。

## 📸 界面预览

| 编辑界面 | 实时预览 |
| --- | --- |
| <img src="https://coresg-normal.trae.ai/api/ide/v1/text_to_image?prompt=A%20screenshot%20of%20a%20modern%20web-based%20resume%20editor%20interface.%20On%20the%20top%20left%2C%20it%20says%20%22%E7%AE%80%E5%8E%86%E7%BC%96%E8%BE%91%E5%99%A8%22%20(Resume%20Editor)%20in%20bold%20black.%20Top%20right%20has%20blue%20action%20links%20with%20plus%20icons%20for%20%22Custom%20Module%22%20and%20%22Custom%20Config%22.%20Below%20is%20a%20horizontal%20tab%20bar%20with%20%22Basic%20Info%22%20active%20(blue%20underline).%20The%20main%20content%20area%20shows%20a%20form%20for%20basic%20information%3A%20a%20centered%20gray%20avatar%20placeholder%20with%20upload%2Fremove%20buttons%2C%20followed%20by%20a%20grid%20of%20input%20fields%20(Name%2C%20Phone%2C%20Email%2C%20Gender)%20with%20icons.%20Bottom%20bar%20shows%20save%20status%20and%20a%20blue%20%22Save%22%20button.%20Clean%2C%20white%20background%2C%20modern%20UI%20style.&image_size=square_hd" alt="简历编辑器界面" width="400"/> | <img src="https://coresg-normal.trae.ai/api/ide/v1/text_to_image?prompt=A%20screenshot%20of%20a%20digital%20resume%20preview%20page.%20The%20layout%20mimics%20an%20A4%20paper%20on%20a%20light%20gray%20background.%20At%20the%20top%2C%20a%20centered%20name%20%22%E5%BC%A0%E4%B8%89%22%20(Zhang%20San)%20in%20large%20bold%20text%2C%20followed%20by%20small%20gray%20personal%20details%20and%20contact%20info.%20Below%20are%20sections%20with%20blue%20headers%3A%20%22Education%22%2C%20%22Internship%22%2C%20%22Projects%22.%20Content%20is%20structured%20cleanly%20with%20black%20text%20and%20right-aligned%20dates.%20Bottom%20right%20has%20floating%20action%20buttons%20for%20%22Edit%22%20and%20%22Export%20PDF%22.%20Professional%20and%20minimalist%20design.&image_size=square_hd" alt="简历实时预览界面" width="400"/> |

## ✨ 核心特性

- **所见即所得 (WYSIWYG)**：左侧编辑面板，右侧 A4 纸张实时预览，修改即刻生效。
- **全屏沉浸式体验**：精心设计的全屏布局，最大化利用屏幕空间，支持响应式缩放与滚动。
- **强大的模块管理**：
  - **拖拽排序**：通过直观的拖拽操作调整简历各模块顺序。
  - **自定义模块**：支持添加任意数量的自定义模块（如“开源贡献”、“校园经历”等）。
  - **显隐控制**：一键切换模块的显示与隐藏状态。
- **Markdown 支持**：所有长文本区域（个人评价、经历描述等）均支持 Markdown 语法，轻松实现排版。
- **高度可配置**：
  - 支持更换简历主题色。
  - 支持调整字体大小、行高、模块间距等排版细节。
  - 支持切换不同的简历模板风格（现代、经典、简约）。
- **PDF 导出**：基于 `html2pdf.js` 的高质量 A4 PDF 导出，保持网页渲染效果。
- **本地存储**：编辑内容自动保存至浏览器 LocalStorage，防止数据丢失。

## 🚀 快速启动

1. **环境准备**：确保已安装 Python 3.x。
2. **安装依赖**：
   ```bash
   pip install django
   ```
3. **运行服务**：
   ```bash
   python manage.py runserver
   ```
4. **访问应用**：
   打开浏览器访问 [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

## 📂 项目结构

- **templates/index.html**: 核心前端文件，包含 Vue.js 逻辑、CSS 样式和 HTML 结构。
- **static/**: 静态资源目录（JS 库、字体图标等）。
- **core/**: Django 应用核心逻辑。
- **PersonalInf/**: Django 项目配置目录。
- **manage.py**: Django 项目管理入口。

## 🛠️ 技术栈

- **前端**: Vue.js 3 (CDN), FontAwesome 5, html2pdf.js, marked.js
- **后端**: Python, Django
- **样式**: 原生 CSS3 (Flexbox 布局, CSS 变量)

## 📝 使用指南

1. **编辑信息**：在左侧面板填写基本信息、教育背景、工作经历等。
2. **调整布局**：点击“自定义简历配置”调整字体、间距和主题色；点击“模块配置”拖拽调整顺序。
3. **添加模块**：点击顶部“+ 自定义简历模块”添加额外的简历板块。
4. **导出简历**：点击右下角“导出 PDF”按钮生成文件。
