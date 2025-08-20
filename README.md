# Zentle - 智能中医健康管理应用

<div align="center">
  <img src="https://img.shields.io/badge/Next.js-15.4.6-black" alt="Next.js">
  <img src="https://img.shields.io/badge/React-19.1.0-blue" alt="React">
  <img src="https://img.shields.io/badge/TypeScript-5.x-blue" alt="TypeScript">
  <img src="https://img.shields.io/badge/TailwindCSS-4.x-38B2AC" alt="TailwindCSS">
  <img src="https://img.shields.io/badge/Node.js-Express-green" alt="Node.js">
  <img src="https://img.shields.io/badge/Database-Supabase-green" alt="Supabase">
</div>

## 📖 项目简介

煦养是一款基于人工智能技术的中医健康管理应用，将传统中医智慧与现代科技相结合，为用户提供个性化的健康管理服务。应用通过智能记录、AI分析和个性化建议，帮助用户建立健康的生活习惯，实现身心和谐。

### 🎯 核心理念

- **内观自省**：通过日常健康记录，培养用户的自我觉察能力
- **顺时养生**：结合节气、天气等外部因素，提供动态的养生建议
- **智能问诊**：基于AI的中医问诊，建立个人体质档案
- **社区互助**：打造健康生活方式的交流社区

## ✨ 主要功能

### 🔍 内观记录
- **多维度健康记录**：睡眠、饮食、情绪、症状等全方位记录
- **智能记录方式**：支持问答模式、自由记录、图片上传等
- **即时AI反馈**：每次记录后获得个性化的中医调理建议
- **历史数据分析**：按日期分组展示，追踪健康变化趋势

### 🌿 顺时养生
- **动态养生方案**：基于节气、天气、个人状态的个性化建议
- **天时地利分析**：结合地理位置和气候变化的养生指导
- **饮食调和建议**：根据体质和当日状态推荐食疗方案
- **经络穴位指导**：针对性的穴位按摩和经络疏通建议

### 🤖 AI智能问诊
- **中医四诊结合**：望闻问切的数字化实现
- **舌诊AI分析**：通过图像识别分析舌象特征
- **体质档案建立**：生成个人中医体质分析报告
- **动态更新机制**：定期更新体质标签，确保建议精准性

### 👥 社区交流
- **内观部落**：健康生活方式的分享社区
- **内容创作**：支持食方、心得、好物等多种笔记类型
- **激励体系**：精进榜、智慧榜、互助榜等排名机制
- **主题活动**：结合节气的定期社区活动

## 🛠️ 技术栈

### 前端技术
- **框架**：Next.js 15.4.6 + React 19.1.0
- **语言**：TypeScript 5.x
- **样式**：TailwindCSS 4.x
- **图标**：Lucide React
- **构建工具**：Turbopack

### 后端技术
- **运行环境**：Node.js
- **框架**：Express.js
- **语言**：TypeScript
- **数据库**：Supabase (PostgreSQL)
- **认证**：JWT + bcryptjs
- **AI集成**：OpenAI API
- **日志**：Winston + Morgan
- **安全**：Helmet + CORS

### 开发工具
- **代码规范**：ESLint + Prettier
- **测试框架**：Jest
- **开发服务器**：Nodemon
- **API文档**：RESTful API

## 🚀 快速开始

### 环境要求
- Node.js >= 18.0.0
- npm >= 8.0.0
- Supabase 账户

### 安装步骤

1. **克隆项目**
```bash
git clone https://github.com/orangellie/Ellie.Xu/health-app.git
cd health-app
```

2. **安装前端依赖**
```bash
npm install
```

3. **安装后端依赖**
```bash
cd backend
npm install
```

4. **环境配置**

在后端目录创建 `.env` 文件：
```env
# Supabase 配置
SUPABASE_URL=your_supabase_url
SUPABASE_ANON_KEY=your_supabase_anon_key
SUPABASE_SERVICE_ROLE_KEY=your_supabase_service_role_key

# JWT 配置
JWT_SECRET=your_jwt_secret

# OpenAI 配置
OPENAI_API_KEY=your_openai_api_key

# 服务器配置
PORT=3001
NODE_ENV=development
```

5. **数据库初始化**
```bash
# 在 Supabase 控制台执行 create_health_records_table.sql
```

6. **启动开发服务器**

启动后端服务：
```bash
cd backend
npm run dev
```

启动前端服务：
```bash
npm run dev
```

7. **访问应用**
- 前端：http://localhost:3000
- 后端API：http://localhost:3001

## 📁 项目结构

```
health-app/
├── src/                    # 前端源码
│   ├── app/               # Next.js App Router
│   │   ├── page.tsx       # 主页面
│   │   ├── consultation/  # 问诊页面
│   │   ├── community/     # 社区页面
│   │   └── profile/       # 个人中心
│   ├── components/        # 可复用组件
│   └── utils/            # 工具函数
│       └── api.ts        # API 接口
├── backend/               # 后端源码
│   ├── src/
│   │   ├── routes/       # 路由定义
│   │   ├── services/     # 业务逻辑
│   │   ├── middleware/   # 中间件
│   │   ├── controllers/  # 控制器
│   │   └── types/        # 类型定义
│   ├── config/           # 配置文件
│   └── utils/            # 工具函数
├── public/               # 静态资源
└── docs/                 # 项目文档
```

## 🔧 开发指南

### 代码规范
- 使用 TypeScript 进行类型安全开发
- 遵循 ESLint 配置的代码规范
- 组件采用函数式组件 + Hooks
- API 接口遵循 RESTful 设计原则

### 提交规范
```bash
# 功能开发
git commit -m "feat: 添加健康记录按日期分组功能"

# 问题修复
git commit -m "fix: 修复时间显示错误"

# 文档更新
git commit -m "docs: 更新 README 文档"
```

### API 接口

主要 API 端点：
- `GET /api/health-records` - 获取健康记录列表
- `POST /api/health-records` - 创建健康记录
- `GET /api/health-records/grouped-by-date` - 按日期分组获取记录
- `POST /api/consultation` - AI 问诊接口
- `GET /api/user/profile` - 获取用户档案

## 🧪 测试

```bash
# 运行前端测试
npm run test

# 运行后端测试
cd backend
npm run test

# 代码检查
npm run lint
```

## 📦 构建部署

### 生产构建
```bash
# 构建前端
npm run build

# 构建后端
cd backend
npm run build
```

### 启动生产服务
```bash
# 启动前端
npm start

# 启动后端
cd backend
npm start
```

## 🤝 贡献指南

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 👥 团队

- **产品设计**：基于中医理论的健康管理产品设计
- **前端开发**：React + Next.js 现代化前端架构
- **后端开发**：Node.js + Express 高性能后端服务
- **AI集成**：OpenAI API 智能问诊与建议生成


<div align="center">
  <p>用心守护每一个人的健康 💚</p>
  <p>让传统中医智慧在数字时代焕发新生 🌿</p>
</div>


