# 私彩内容后台系统 + 动态随机子域名网关系统

> ✈️：@dinggui98  
> 版本：v1.2.4 (2026-07-19)  
> 定位：澳门/香港彩票资讯站 + 防封动态网关

---

## 截图预览

### 前端页面

![前端01](前端01.png)
![前端02](前端02.png)
![前端03](前端03.png)
![前端04](前端04.png)
![前端05](前端05.png)

### 后台管理

![后台管理01](后台管理01.png)
![后台管理02](后台管理02.png)
![后台管理03](后台管理03.png)
![后台管理04](后台管理04.png)
![后台管理05](后台管理05.png)
![后台管理06](后台管理06.png)
![后台管理07](后台管理07.png)
![后台管理08](后台管理08.png)
![后台管理09](后台管理09.png)
![后台管理10](后台管理10.png)
![后台管理11](后台管理11.png)
![后台管理12](后台管理12.png)
![后台管理13](后台管理13.png)
![后台管理14](后台管理14.png)
![后台管理15](后台管理15.png)
![后台管理16](后台管理16.png)
![后台管理17](后台管理17.png)
![后台管理18](后台管理18.png)
![后台管理19](后台管理19.png)
![后台管理20](后台管理20.png)
![后台管理21](后台管理21.png)

### 私彩统计器

![私彩统计器01](私彩统计器01.png)
![私彩统计器02](私彩统计器02.png)
![私彩统计器03](私彩统计器03.png)
![私彩统计器04](私彩统计器04.png)
![私彩统计器05](私彩统计器05.png)
![私彩统计器06](私彩统计器06.png)
![私彩统计器07](私彩统计器07.png)
![私彩统计器08](私彩统计器08.png)

---

## 技术栈

| 层 | 技术 |
|--|--|
| 后端 | Node.js + NestJS 11 + TypeScript |
| 数据库 | PostgreSQL（Prisma ORM 5.8） |
| 缓存 | Redis（ioredis，含内存降级） |
| 后台前端 | Vue 3.4 + Vite 5 + Element Plus 2.5 + Pinia |
| 对外前端 | 原生 HTML/CSS/JS |
| 实时通信 | Socket.IO + 原生 WebSocket |
| 爬虫 | Puppeteer 24.x |
| OCR | OpenAI 兼容 API |
| 部署 | PM2 + Nginx + 宝塔面板 |

## 核心子系统

1. **后台管理系统** — 基于 RBAC 的权限管理（Vue 3 + Element Plus）
2. **内容管理系统** — NestJS + PostgreSQL + Redis
3. **安全体系** — JWT 双令牌、TOTP 两步验证、登录锁定、IP 白名单、审计日志、速率限制
4. **彩票系统** — 开奖记录、批量导入、WebSocket 实时开奖、倒计时推送
5. **代理/订单系统** — 分层代理、结算费率、订单批次、盈亏报表、热力图
6. **动态随机子域名网关系统** — 防封随机子域名、Redis 映射、302 跳转、风控检查
7. **防火墙/风控** — IP/UA/Referer 黑名单
8. **爬虫/自动采集** — 定时任务、Puppeteer、MD5 去重
9. **域名管理** — 主域名/泛域名注册
10. **小助手 (New-Order-Acquisition-Assistant)** — 移动端收单、OCR 识别、智能输入
11. **对外前端** — 动态渲染、广告格子、轮播、跑马灯、iframe 嵌入

## 数据库模型 (24 个)

| 模块 | 模型 |
|--|--|
| 权限 | User, Role, UserRole, Module, Permission, RolePermission |
| 内容 | Content, PeriodConfig |
| 站点 | SiteSetting, PageLayout |
| 安全 | AuditLog, FirewallRule |
| 网关 | Domain, Route, RouteSubdomain, GatewayLog |
| 代理订单 | Agent, AgentSession, AgentBan, AgentLoginLog, OrderBatch, OrderItem |
| 彩票 | LotteryRecord |
| 上传 | UploadFile, UploadImage, ImageCategory |
| 爬虫 | SpiderTask, SpiderImage, SpiderLog |
