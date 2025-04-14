# 照片风格转换网站

这是一个基于AI技术的照片风格转换网站，用户可以上传照片，选择预设风格，系统会使用OpenAI的图像处理API将照片转换为选定的艺术风格，并通过电子邮件发送结果给用户。

## 功能特点

- 多种预设艺术风格选择（梵高风格、赛博朋克、水墨画、动漫化等）
- 简单直观的用户界面
- 拖放式图片上传
- 通过电子邮件接收处理结果
- 完全基于前端和Serverless架构，无需传统后端服务器

## 技术栈

- **前端**: React, Vite
- **UI组件**: 自定义CSS样式
- **文件处理**: react-dropzone
- **API请求**: axios
- **Serverless函数**: Vercel Serverless Functions
- **图像处理**: OpenAI API
- **邮件发送**: SendGrid API

## 本地开发

### 前提条件

- Node.js (v14+)
- npm 或 yarn
- OpenAI API密钥
- SendGrid API密钥

### 安装步骤

1. 克隆仓库

```bash
git clone <repository-url>
cd photo-style-transfer
```

2. 安装依赖

```bash
npm install
```

3. 创建环境变量文件 `.env.local`

```
OPENAI_API_KEY=your_openai_api_key
SENDGRID_API_KEY=your_sendgrid_api_key
```

4. 启动开发服务器

```bash
npm run dev
```

5. 在浏览器中访问 `http://localhost:3000`

## 部署

### 使用Vercel部署

1. 在Vercel上创建一个新项目
2. 连接到你的Git仓库
3. 在环境变量设置中添加：
   - `OPENAI_API_KEY`
   - `SENDGRID_API_KEY`
4. 部署项目

### 使用Netlify部署

1. 在Netlify上创建一个新项目
2. 连接到你的Git仓库
3. 设置构建命令为 `npm run build`
4. 设置发布目录为 `dist`
5. 在环境变量设置中添加：
   - `OPENAI_API_KEY`
   - `SENDGRID_API_KEY`
6. 部署项目

## 注意事项

- OpenAI API和SendGrid API都需要付费使用
- 确保安全存储API密钥，不要将其暴露在前端代码中
- 图像处理可能需要一些时间，取决于OpenAI API的响应速度
- 建议限制上传图片的大小，以提高处理速度和减少API成本

## 隐私政策

- 上传的照片仅用于风格转换处理
- 电子邮件地址仅用于发送处理结果
- 不会永久存储用户的照片或个人信息

## 许可证

MIT