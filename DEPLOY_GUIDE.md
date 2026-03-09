# GitHub Pages 部署快速指南

## 🎯 5 分钟完成部署

### 方案一：网页上传（最简单）⭐

#### 1️⃣ 创建 GitHub 仓库
1. 访问 https://github.com
2. 登录账号（没有就注册一个，免费）
3. 点击右上角 **"+"** → **"New repository"**
4. 填写信息：
   - Repository name: `pdf-to-image`（或任意名字）
   - ✅ 选择 **"Public"**
   - ❌ 不要勾选 "Initialize this repository with a README"
5. 点击 **"Create repository"**

#### 2️⃣ 上传文件
1. 在仓库页面，点击 **"uploading an existing file"**
2. 打开文件夹：`D:\File\python_file\tools\File_Format_Conversion`
3. 将 `pdf_to_image.html` 拖到上传区域
4. **重要**：上传后把文件名改为 `index.html`
5. 点击 **"Commit changes"**

#### 3️⃣ 启用 GitHub Pages
1. 在仓库页面，点击 **"Settings"**（设置）
2. 左侧菜单找到并点击 **"Pages"**
3. 在 "Build and deployment" 下：
   - Source: 选择 **"Deploy from a branch"**
   - Branch: 选择 **"main"**，文件夹选 **"/ (root)"**
4. 点击 **"Save"**

#### 4️⃣ 等待部署完成
- 等待 1-2 分钟
- 刷新 Pages 页面
- 看到绿色对勾和网址即成功！

#### 5️⃣ 分享您的工具
访问地址格式：
```
https://你的 GitHub 用户名.github.io/仓库名/
```

例如：
```
https://zhangsan.github.io/pdf-to-image/
```

---

### 方案二：Git 命令行（适合熟悉 Git 的用户）

```bash
# 进入项目目录
cd D:\File\python_file\tools\File_Format_Conversion

# 复制并重命名文件
copy pdf_to_image.html index.html

# 初始化 Git（如果还没有）
git init

# 添加所有文件
git add index.html server.py requirements.txt .gitignore

# 提交
git commit -m "Deploy PDF to image tool to GitHub Pages"

# 创建 main 分支
git branch -M main

# 在 GitHub 创建仓库后，关联远程仓库
# （替换为您的实际仓库地址）
git remote add origin https://github.com/你的用户名/pdf-to-image.git

# 推送到 GitHub
git push -u origin main
```

然后按方案一的步骤 3 启用 Pages 即可。

---

## ✅ 部署后效果

### 功能特性
- ✅ 全球可访问（有网络就行）
- ✅ 24 小时在线
- ✅ 自动 HTTPS 加密
- ✅ 免费使用 CDN 加速
- ✅ 无需自己电脑运行
- ✅ 支持所有现代浏览器

### 访问示例
假设您的 GitHub 用户名是 `zhangsan`，仓库名是 `pdf-to-image`：

**访问地址：**
```
https://zhangsan.github.io/pdf-to-image/
```

把这个链接发给任何人，他们都能使用！

---

## 🔧 常见问题

### Q1: 部署后页面空白或报错？
**A:** 检查以下几点：
- 确保文件名是 `index.html`（不是 pdf_to_image.html）
- 打开浏览器控制台（F12）查看错误信息
- 确认网络能访问 cdnjs.cloudflare.com

### Q2: 国内访问慢怎么办？
**A:** 使用 Vercel 部署：
1. 访问 https://vercel.com
2. 用 GitHub 账号登录
3. 导入刚才的仓库
4. 点击 Deploy
5. 获得更快的国内访问域名

### Q3: 如何更新代码？
**A:** 
- 网页版：在 GitHub 上直接编辑文件或重新上传
- Git 版：修改后执行 `git push` 即可

### Q4: 可以自定义域名吗？
**A:** 可以！在 Pages 设置的 "Custom domain" 中添加您的域名。

### Q5: 文件大小有限制吗？
**A:** 
- GitHub 仓库限制：单个文件最大 100MB
- 工具本身限制：用户可上传最大 50MB 的 PDF

---

## 💡 优化建议

### 1. 添加描述文件
在仓库根目录创建 `README.md`：

```markdown
# 📄 PDF 转图片工具

一个简单好用的在线 PDF 转图片工具

## ✨ 功能特性
- 支持拖拽上传
- 转换为 PNG/JPG 格式
- 单张下载或批量打包
- 响应式设计

## 🚀 使用方法
直接访问：https://你的用户名.github.io/pdf-to-image/
```

### 2. 添加许可证
在仓库中点击 "Add file" → "Create new file"
命名为 `LICENSE`，选择 MIT License

### 3. 设置仓库标签
在仓库主页右侧添加 topics：
`pdf`, `image-converter`, `javascript`, `tool`

---

## 🎉 总结

**GitHub Pages 是最适合的部署方案，因为：**

✅ 完全免费  
✅ 永久在线  
✅ 无需云服务器  
✅ 设置简单（5 分钟搞定）  
✅ 全球可访问  
✅ 自动 HTTPS  
✅ 速度快（CDN 加速）  

**立即开始：**
1. 去 GitHub 创建仓库
2. 上传 index.html
3. 启用 Pages
4. 分享链接给朋友

就这么简单！🚀
