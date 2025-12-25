# INCON Group 网站内容更新指南 (Collaborator Guide)

## 开始：添加一篇文章的流程

添加文章主要分为三个步骤：**准备资源文件** -> **上传文件** -> **修改 HTML 代码**。

### 1. 准备并放置资源文件

为了保持路径一致，请务必将文件放在以下指定目录中：

* **文章预览图 & 论文 PDF**：统一放在 `doc/[子页面关键词]/p/`（已发表）或 `doc/[子页面关键词]/ur/`（审稿中）目录下。预览图和paper名可为 pic01 & paper01, pic02 & paper02。
* *关键词对应表*：`mri` (Neuroimaging), `tissue` (Tissue Imaging), `gene` (Imaging Genetics), `demo` (Clinical Translation)。


### 2. 修改子页面 HTML

打开对应的子页面文件：

* `page_mri/index.html`
* `page_tissue/index.html`
* `page_gene/index.html`
* `page_demo/index.html`

### 3. 代码模板 (直接粘贴)

在 `<ul>` 标签内的对应位置（`Published Works` 或 `Under Review`）添加以下 `<li>` 块：

```html
<li class="paper-item">
    <img src="doc/[子页面关键词]/论文状态子文件夹/你的图片名.png" alt="Preview" class="paper-preview-img">
    
    <div class="paper-content">
        <span class="paper-title">这里输入你的论文标题</span>
        <span class="paper-journal">发表/投稿期刊（预印本写Preprint）</span>
        <span class="paper-author">作者姓名</span>
        
        <p class="paper-desc">请简要描述这项工作的核心创新点和贡献（建议 2-3 句话）。</p>
        
        <div class="paper-links">
            <a href="doc/[子页面关键词]/论文状态子文件夹/你的论文.pdf" target="_blank">Paper</a> |
            <a href="https://github.com/..." target="_blank">Code</a>
        </div>
    </div>
</li>

```

---

## 🛠 关键目录结构说明

协作者需要关注的目录树如下：

```text
INPN/
├── assets/
│   ├── poster/         <-- 废弃文件夹，不需要修改
│   └── main.css        <-- 全局样式（通常不需要修改）
├── doc/
│   ├── mri/            <-- Neuroimaging 页面图片 & 论文PDF文件
│   ├── tissue/         <-- Tissue Imaging 页面图片 & 论文PDF文件
│   ├── gene/           <-- Imaging Genetics 页面图片 & 论文PDF文件
│   └── demo/           <-- Clinical Translation 页面图片 & 论文PDF文件
├── page_xxx/
│   └── index.html      <-- 各个子页面的代码，上传后需要在这里修改文字描述并对应路径
└── index.html          <-- 网站主页

```

---

## ⚠️ 注意事项（必读）

1. **路径一致性**：子页面中都有 `<base href="..">` 标签，这意味着在子页面 HTML 里写路径时，应以项目根目录为基准（例如直接写 `doc/...` 而不是 `../doc/...`）。
2. **图片规格**：建议使用 `.png` 或 `.jpg` 格式，预览图会自动裁剪为 `180x120px`。为了显示效果，请尽量使用横向比例的图片。
```


**核心原因**：采用这种结构化的添加方式，可以确保新内容能够自动适配移动端布局，并保持学术站点严谨、统一的视觉风格。



