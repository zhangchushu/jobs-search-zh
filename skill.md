---
name: mcp-jobs-job-search
description: 使用 mcp-jobs（MCP 多平台职位聚合服务）搜索国内岗位并获取职位详情；支持关键词/城市/薪资/年限筛选，输出标准化结果表。
version: 1.0.0
metadata:
  openclaw:
    requires:
      bins:
        - node
        - npx
    # 这些是可选项：mcp-jobs 不需要任何 env 也能跑，但如果你要启用鉴权/调试/浏览器参数，可在运行 mcp-jobs 时注入
    # 这里写出来，方便安全审计与用户理解（不会强制要求）
    # requires:
    #   env:
    #     - USERNAME
    #     - PASSWORD
    #     - CRAWLER_HEADLESS
    #     - CRAWLER_TIMEOUT
    #     - CRAWLER_VIEWPORT_WIDTH
    #     - CRAWLER_VIEWPORT_HEIGHT
    #     - CRAWLER_DEBUG
    emoji: "🧭"
    homepage: https://github.com/mergedao/mcp-jobs
---

# mcp-jobs 求职搜索 Skill（OpenClaw）

本 skill 教你如何让 OpenClaw 通过 **mcp-jobs** MCP 服务完成两类任务：

1) **搜索职位列表**（多平台聚合）  
2) **获取某个职位链接的详细信息**

---

## 依赖与启动（一次性准备）

### 1) 启动 mcp-jobs（零配置）
在终端运行：

```bash
npx -y mcp-jobs