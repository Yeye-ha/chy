

# 基于 Spring Boot 的校园宿舍后勤维修管理系统。

学生微信小程序提交报修，师傅微信小程序接单处理，Vue 管理后台统一调度与数据统计。

## 技术栈

| 层 | 技术 |
|---|---|
| 前端（管理后台） | Vue 3 + Vite 5 + Pinia + Element Plus + ECharts |
| 前端（移动端） | 原生微信小程序 + Vant Weapp |
| 后端 | Spring Boot 3.2 + Spring Security + JWT + MyBatis-Plus |
| 数据库 | MySQL 8.x（Navicat 管理） |
| 运行环境 | JDK 21 + Maven 3.8+ + Node.js 18+ |
| 开发工具 | IDEA + VS Code + Postman |

## 功能模块

- **学生端（小程序）**：微信授权登录、绑定楼栋房间、报修下单（多图上传）、工单列表与状态筛选、工单详情时间线、完工评价、站内消息
- **师傅端（小程序）**：工单池与匹配得分、接单 / 标记上门 / 上传完工照片、进行中与历史工单、个人工作量与评分统计
- **管理后台（Web）**：数据看板（核心指标、楼栋热力图、故障趋势）、工单管理（手动派单、异常工单处理）、楼栋房间管理、师傅账号与技能标签管理、故障类型配置、派单权重与超时改派规则配置、用户管理与操作日志

# vs code 环境
```powershell
确认版本
node -v
npm -v
```
<img width="391" height="161" alt="image" src="https://github.com/user-attachments/assets/c17ac02b-4bce-4081-b4e8-8236538d881b" />


安装插件：

- Vue - Official
- Prettier - Code formatter
- ESLint
- HTML CSS Support
- Chinese (Simplified) Language Pack（中文界面，可选）




## 快速开始

```bash
# 1. 导入数据库脚本
mysql -u root -p < sql/campus_repair.sql

# 2. 启动后端
cd server
mvn spring-boot:run

# 3. 启动管理后台
cd admin
npm install
npm run dev

# 4. 小程序：微信开发者工具导入 miniprogram 目录
```

## 目录结构

```
├── server/        # Spring Boot 后端
├── admin/         # Vue 3 管理后台
├── miniprogram/   # 微信小程序（学生端 + 师傅端）
└── sql/           # 数据库脚本
```
