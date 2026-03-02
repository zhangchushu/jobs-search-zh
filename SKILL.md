---
name: mcp-jobs-job-search
description: |
  使用 mcp-jobs（MCP 多平台职位聚合）搜索国内岗位并获取职位详情。
  ✅ 工具名已对齐 mcp-jobs 实际暴露的 MCP tools：mcp_search_job / mcp_job_detail
version: 1.1.0
emoji: "🧭"
tags: ["job-search", "mcp", "recruitment", "china"]
requirements:
  mcp_servers:
    - name: mcp-jobs
      command: npx
      args: ["-y", "mcp-jobs"]
---

# mcp-jobs 求职 Skill（OpenClaw）

> 如果你遇到“工具不存在”，99% 是因为工具名写错了。  
> mcp-jobs 实际提供的工具是：`mcp_search_job` 与 `mcp_job_detail`。  
> （内部函数 `searchJobList/crawlJobDetail` 不是 MCP tool，不能被客户端直接调用。）

---

## 0) 一次性准备（必须做对）

### A. 启动 MCP Server（本地终端）
```bash
npx -y mcp-jobs
