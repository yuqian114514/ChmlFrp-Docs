---
layout: home

hero:
  name: "ChmlFrp 内网穿透"
  text: "教程文档"
  tagline: 支持 Windows/macOS/Linux/安卓/路由器，免费、高速、稳定、不限流量。
  actions:
    - theme: brand
      text: 查阅文档 →
      link: /docs
      icon: ⚡️
    - theme: alt
      text: 立即使用
      link: https://www.chmlfrp.net
      icon: 📦
      target: _blank
    - theme: alt
      text: 加入社区
      link: /community
      icon: 💬

features:
  - icon: 🚀
    title: 极简配置
    details: 几步完成映射，无需复杂网络知识
  - icon: 🌐
    title: 全平台支持
    details: Windows/macOS/Linux/freeBSD/安卓/OpenWRT 全兼容
  - icon: 🔒
    title: 加密传输
    details: TLS 加密通道保障数据安全
  - icon: 🛠️
    title: 开发者友好
    details: 提供 API 和 Webhook 集成能力
  - icon: 📈
    title: 不限流量
    details: 免费且不限流量使用，无需担心流量耗尽问题，让您的应用持续在线。
  - icon: 🎨
    title: 清爽无广
    details: 完全无广告的清爽体验，采用naiveui开发的控制面板，功能强大，简约美观
---

<script setup>
import { onMounted, ref } from 'vue'

const stats = ref({
  nodes: 0,
  tunnels: 0,
  users: 0
})

const fetchStats = async () => {
  try {
    const res = await fetch('https://cf-v2.uapis.cn/panelinfo')
    const data = await res.json()
    stats.value = {
      nodes: data.data.node_amount || 0,
      tunnels: data.data.tunnel_amount || 0,
      users: data.data.user_amount || 0
    }
  } catch (err) {
    console.error('Failed to fetch stats', err)
    stats.value = { nodes: 35, tunnels: 55000, users: 50000 }
  }
}

onMounted(() => {
  fetchStats()
})
</script>

<style>
.stats-container {
  display: flex;
  justify-content: space-around;
  margin: 2rem auto;
  /* max-width: 800px; */
  width: 100%;
  padding: 1.5rem;
  background: var(--vp-c-bg-soft);
  border-radius: 12px;
  box-shadow: var(--vp-shadow-1);
  transition: background-color 0.5s ease;
}

.stat-item {
  text-align: center;
  padding: 0 1.5rem;
}

.stat-value {
  font-size: 2.5rem;
  font-weight: 700;
  color: var(--vp-c-brand);
  margin-bottom: 0.5rem;
  font-family: 'Dosis', sans-serif;
  transition: color 0.5s ease;
}

.stat-label {
  font-size: 1rem;
  color: var(--vp-c-text-2);
  font-weight: 500;
  transition: color 0.5s ease;
}

@media (max-width: 640px) {
  .stats-container {
    flex-direction: column;
    gap: 1.5rem;
  }
  
  .stat-item {
    padding: 0;
  }
  
  .stat-value {
    font-size: 2rem;
  }
}
</style>

<div class="stats-container">
  <div class="stat-item">
    <div class="stat-value" v-text="stats.nodes"></div>
    <div class="stat-label">全球节点</div>
  </div>
  <div class="stat-item">
    <div class="stat-value" v-text="stats.tunnels"></div>
    <div class="stat-label">活跃隧道</div>
  </div>
  <div class="stat-item">
    <div class="stat-value" v-text="stats.users"></div>
    <div class="stat-label">注册用户</div>
  </div>
</div>

::: tip
欢迎参与文档共建！您的每一个PR都是对我们莫大的帮助。请访问GitHub仓库提交改进建议。我们将定期审核合并，并为杰出贡献者提供VIP等专属福利。
:::