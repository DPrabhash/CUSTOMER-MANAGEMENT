<template>
  <q-page class="bg-black text-white">
    <!-- Hero Section -->
    <section id="hero" class="hero-section relative-position flex flex-center q-pa-md">
      <div class="absolute-full" :style="heroBackgroundStyle"></div>
      <div class="container relative-position z-top w-full">
        <div class="row items-center q-col-gutter-xl">
          <!-- Text Content (Left) -->
          <div class="col-12 col-md-5 text-left">
            <div
              class="q-mb-md text-primary text-uppercase text-weight-bold tracking-widest fade-in-up text-subtitle1"
            >
              Next Gen CRM
            </div>
            <h1
              class="text-h2 q-mt-none q-mb-md text-weight-bolder hero-title fade-in-up delay-100"
              style="line-height: 1.1"
            >
              Manage Customers <br />
              <span class="text-transparent bg-clip-text bg-gradient-red">Like A Pro</span>
            </h1>
            <p class="text-h6 text-grey-4 q-mb-xl fade-in-up delay-200 text-weight-light">
              The all-in-one platform to track, engage, and grow your customer base. Powerful
              analytics, seamless automation, and intuitive design.
            </p>
            <div class="row justify-start q-gutter-md fade-in-up delay-300 no-wrap">
              <q-btn
                unelevated
                color="primary"
                size="lg"
                label="Start Free Trial"
                padding="12px 36px"
                class="text-weight-bold"
              />
              <q-btn
                outline
                color="white"
                size="lg"
                label="View Demo"
                padding="12px 36px"
                class="text-weight-bold"
              />
            </div>
          </div>

          <!-- Image Content (Right) -->
          <div class="col-12 col-md-7">
            <div class="fade-in-up delay-400 relative-position">
              <div class="dashboard-glare"></div>
              <q-card
                dark
                class="bg-transparent no-shadow hero-image-card"
                style="border: 1px solid #333; border-radius: 12px; overflow: hidden"
              >
                <q-img
                  src="~assets/crm_dashboard.png"
                  fit="contain"
                  style="
                    border: 1px solid #333;
                    border-radius: 12px;
                    box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5);
                  "
                  :ratio="16 / 9"
                />
              </q-card>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Stats Section -->
    <section id="stats" class="q-py-xl bg-dark-page borders-y-red">
      <div class="container q-px-md">
        <div class="row q-col-gutter-lg text-center">
          <div class="col-12 col-md-3">
            <div class="text-h3 text-weight-bolder text-white">10k+</div>
            <div class="text-subtitle1 text-primary text-uppercase">Active Users</div>
          </div>
          <div class="col-12 col-md-3">
            <div class="text-h3 text-weight-bolder text-white">99.9%</div>
            <div class="text-subtitle1 text-primary text-uppercase">Uptime</div>
          </div>
          <div class="col-12 col-md-3">
            <div class="text-h3 text-weight-bolder text-white">24/7</div>
            <div class="text-subtitle1 text-primary text-uppercase">Support</div>
          </div>
          <div class="col-12 col-md-3">
            <div class="text-h3 text-weight-bolder text-white">50+</div>
            <div class="text-subtitle1 text-primary text-uppercase">Integrations</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="q-py-xl relative-position">
      <div class="container q-px-md">
        <div class="text-center q-mb-xl">
          <h2 class="text-h3 text-weight-bold q-mb-sm">Powerful Features</h2>
          <p class="text-grey-5 text-h6">Everything you need to manage relationships.</p>
        </div>

        <div class="row q-col-gutter-xl">
          <!-- Feature 1 -->
          <div class="col-12 col-md-4">
            <q-card dark class="feature-card bg-grey-10 full-height no-shadow overflow-hidden">
              <q-img src="~assets/analytics_feature.png" height="200px" fit="cover" />
              <q-card-section class="q-pa-lg text-center">
                <div class="text-h5 text-weight-bold q-mb-sm">Advanced Analytics</div>
                <p class="text-grey-5">
                  Gain deep insights into customer behavior with our real-time dashboard and
                  predictive reports.
                </p>
              </q-card-section>
            </q-card>
          </div>

          <!-- Feature 2 -->
          <div class="col-12 col-md-4">
            <q-card dark class="feature-card bg-grey-10 full-height no-shadow overflow-hidden">
              <q-img src="~assets/collaboration_feature.png" height="200px" fit="cover" />
              <q-card-section class="q-pa-lg text-center">
                <div class="text-h5 text-weight-bold q-mb-sm">Team Collaboration</div>
                <p class="text-grey-5">
                  Work together seamlessly. Share detailed customer notes, tasks, and pipelines with
                  your team.
                </p>
              </q-card-section>
            </q-card>
          </div>

          <!-- Feature 3 -->
          <div class="col-12 col-md-4">
            <q-card dark class="feature-card bg-grey-10 full-height no-shadow overflow-hidden">
              <q-img src="~assets/automation_feature.png" height="200px" fit="cover" />
              <q-card-section class="q-pa-lg text-center">
                <div class="text-h5 text-weight-bold q-mb-sm">Fast Automation</div>
                <p class="text-grey-5">
                  Automate repetitive tasks. Send emails, update statuses, and trigger workflows
                  instantly.
                </p>
              </q-card-section>
            </q-card>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section id="pricing" class="q-py-xl bg-primary relative-position overflow-hidden">
      <div class="absolute-full pattern-overlay"></div>
      <div class="container q-px-md text-center relative-position z-top">
        <h2 class="text-h3 text-weight-bolder text-white q-mb-md">Ready to Scale?</h2>
        <p class="text-h6 text-white q-mb-xl opacity-80" style="max-width: 600px; margin: 0 auto">
          Join thousands of businesses efficiently managing their customers today.
        </p>
        <q-btn
          unelevated
          color="black"
          text-color="white"
          size="lg"
          label="Get Started Now"
          padding="16px 48px"
          class="text-weight-bold shadow-10"
        />
      </div>
    </section>
  </q-page>
</template>

<script setup>
import { ref, computed, onMounted, onUnmounted } from 'vue'

const mouseX = ref(0)
const mouseY = ref(0)

function handleMouseMove(event) {
  mouseX.value = event.clientX
  mouseY.value = event.clientY
}

onMounted(() => {
  window.addEventListener('mousemove', handleMouseMove)
})

onUnmounted(() => {
  window.removeEventListener('mousemove', handleMouseMove)
})

const heroBackgroundStyle = computed(() => {
  return {
    background: `radial-gradient(circle 1000px at ${mouseX.value}px ${mouseY.value}px, rgba(60, 0, 0, 0.4) 0%, #000000 70%)`,
  }
})

// Index Page
</script>

<style lang="scss" scoped>
.container {
  max-width: 1200px;
  margin: 0 auto;
}

.hero-section {
  min-height: 100vh;
  padding-top: 100px;
  padding-bottom: 50px;
}

.hero-bg {
  background: radial-gradient(circle at center, #220000 0%, #000000 70%);
}

.bg-gradient-red {
  background: linear-gradient(to right, #ffffff, #d50000);
}

.bg-clip-text {
  -webkit-background-clip: text;
}

.text-transparent {
  color: transparent;
}

.borders-y-red {
  border-top: 1px solid #333;
  border-bottom: 1px solid #333;
}

.feature-card {
  border: 1px solid #222;
  transition:
    transform 0.3s,
    border-color 0.3s;

  &:hover {
    transform: translateY(-10px);
    border-color: $primary;

    .icon-box {
      transform: scale(1.1);
    }
  }
}

.icon-box {
  transition: transform 0.3s;
}

.dashboard-glare {
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(213, 0, 0, 0.15) 0%, rgba(0, 0, 0, 0) 60%);
  pointer-events: none;
  z-index: 0;
}

.pattern-overlay {
  background-image:
    linear-gradient(45deg, rgba(0, 0, 0, 0.05) 25%, transparent 25%),
    linear-gradient(-45deg, rgba(0, 0, 0, 0.05) 25%, transparent 25%),
    linear-gradient(45deg, transparent 75%, rgba(0, 0, 0, 0.05) 75%),
    linear-gradient(-45deg, transparent 75%, rgba(0, 0, 0, 0.05) 75%);
  background-size: 20px 20px;
}

.hero-image-card {
  transform: scale(1.15);
  transform-origin: center center;
  transition: transform 0.6s cubic-bezier(0.25, 0.8, 0.25, 1);
  z-index: 10;

  &:hover {
    transform: scale(1.18) translateY(-10px);
    z-index: 20; /* Ensure it pops over everything */
  }
}

/* Animations */
.fade-in-up {
  opacity: 0;
  animation: fadeInUp 0.8s ease-out forwards;
}

.delay-100 {
  animation-delay: 0.1s;
}
.delay-200 {
  animation-delay: 0.2s;
}
.delay-300 {
  animation-delay: 0.3s;
}
.delay-400 {
  animation-delay: 0.4s;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.bg-dark-page {
  background-color: #050505;
}
</style>
