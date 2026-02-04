<script setup lang="ts">
import DefaultTheme from 'vitepress/theme'
import ProgressBar from './components/ProgressBar.vue'
import PageContributors from '../components/PageContributors.vue'

const { Layout } = DefaultTheme

function goBack(): void {
  history.back()
}

function reloadPage(): void {
  location.reload()
}
</script>

<template>
  <Layout>
    <template #layout-top>
      <ProgressBar />

      <div class="background-decoration">
        <div class="decoration-circle circle-1"></div>
        <div class="decoration-circle circle-2"></div>
        <div class="decoration-circle circle-3"></div>
      </div>
    </template>
    <template #doc-after>
      <PageContributors />
    </template>
    <template #not-found>
      <div class="not-found-container">
        <h1 class="not-found-title">404</h1>
        <p class="not-found-desc">Page not found</p>
        <div class="not-found-actions">
          <a href="/" class="not-found-link primary">Go to Home</a>
          <button @click="goBack" class="not-found-link secondary">Go Back</button>
        </div>
        <p class="not-found-hint">
          If you're experiencing persistent 404 errors, try clearing your browser cache or
          <a href="javascript:void(0)" @click="reloadPage">refreshing the page</a>.
        </p>
      </div>
    </template>
  </Layout>
</template>

<style>
.not-found-container {
  padding: 100px 24px;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 60vh;
}

.not-found-title {
  font-size: 8rem;
  font-weight: 700;
  background: var(--custom-gradient);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  margin: 0;
  line-height: 1;
}

.not-found-desc {
  font-size: 2rem;
  font-weight: 500;
  margin: 1rem 0 2rem;
}

.not-found-link {
  display: inline-block;
  background: var(--custom-gradient);
  color: white;
  padding: 0.75rem 1.5rem;
  border-radius: 8px;
  font-weight: 600;
  text-decoration: none;
  transition: all 0.3s ease;
  box-shadow: 0 4px 10px rgba(138, 43, 226, 0.5);
}

.not-found-link:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 15px rgba(138, 43, 226, 0.6);
}

.not-found-actions {
  display: flex;
  gap: 1rem;
  margin-bottom: 2rem;
}

.not-found-link.secondary {
  background: transparent;
  border: 2px solid var(--vp-c-brand-1);
  color: var(--vp-c-brand-1);
  box-shadow: none;
}

.not-found-link.secondary:hover {
  background: rgba(var(--vp-c-brand-1-rgb), 0.1);
  transform: translateY(-3px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.not-found-hint {
  font-size: 0.9rem;
  opacity: 0.8;
  max-width: 400px;
  margin: 0 auto;
}

.not-found-hint a {
  color: var(--vp-c-brand-1);
  text-decoration: underline;
  text-decoration-style: dotted;
}

.background-decoration {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  overflow: hidden;
  pointer-events: none;
}

.decoration-circle {
  position: absolute;
  border-radius: 50%;
  opacity: 0.3;
  filter: blur(60px);
}

.circle-1 {
  background: var(--vp-c-brand-1);
  width: 400px;
  height: 400px;
  top: -100px;
  right: -100px;
}

.circle-2 {
  background: var(--custom-accent);
  width: 300px;
  height: 300px;
  bottom: -50px;
  left: -50px;
}

.circle-3 {
  background: var(--vp-c-brand-2);
  width: 200px;
  height: 200px;
  top: 40%;
  right: -50px;
}

.dark .circle-1 {
  opacity: 0.15;
}

.dark .circle-2 {
  opacity: 0.15;
}

.dark .circle-3 {
  opacity: 0.15;
}

.page-divider {
  height: 1px;
  background: var(--vp-c-divider);
  margin: 2rem 0;
  position: relative;
  overflow: hidden;
}

.page-divider::after {
  content: '';
  position: absolute;
  width: 100px;
  height: 2px;
  background: var(--custom-gradient);
  top: 0;
  left: 50%;
  transform: translateX(-50%);
}
</style>
