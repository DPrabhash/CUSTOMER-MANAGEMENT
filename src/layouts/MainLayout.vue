<template>
  <q-layout view="lHh Lpr lFf" class="bg-black text-white">
    <q-header elevated class="bg-black text-white" style="border-bottom: 2px solid #d50000">
      <q-toolbar class="q-py-md">
        <q-btn flat no-caps no-wrap class="q-ml-xs" to="/">
          <q-avatar size="32px">
            <img src="/icons/logo.png" />
          </q-avatar>
          <q-toolbar-title shrink class="text-weight-bold q-ml-sm">
            CUST<span class="text-primary">MGT</span>
          </q-toolbar-title>
        </q-btn>

        <q-space />

        <div class="q-gutter-sm row items-center no-wrap gt-sm">
          <q-btn flat class="text-white nav-btn" label="Home" @click="scrollToSection('hero')" />
          <q-btn
            flat
            class="text-white nav-btn"
            label="Features"
            @click="scrollToSection('features')"
          />
          <q-btn flat class="text-white nav-btn" label="Stats" @click="scrollToSection('stats')" />
          <q-btn
            flat
            class="text-white nav-btn"
            label="Pricing"
            @click="scrollToSection('pricing')"
          />
          <q-btn outline color="primary" label="Log In" class="q-ml-sm nav-btn-outline" />
          <q-btn
            unelevated
            color="primary"
            label="Get Started"
            class="q-ml-sm text-black text-weight-bold scale-hover"
          />
        </div>

        <q-btn flat round dense icon="menu" class="lt-md" />
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />

      <footer class="bg-black text-white q-py-lg" style="border-top: 1px solid #333">
        <div class="container q-pa-md">
          <div class="row q-col-gutter-xl">
            <div class="col-12 col-md-4">
              <div class="text-h6 text-weight-bold q-mb-md">
                CUST<span class="text-primary">MGT</span>
              </div>
              <p class="text-grey-5">
                The ultimate solution for managing your customer relationships efficiently and
                effectively. Elevate your business with our premium tools.
              </p>
            </div>
            <div class="col-6 col-md-2">
              <div class="text-subtitle1 text-weight-bold q-mb-sm">Product</div>
              <div class="text-grey-5 column q-gutter-ys-sm cursor-pointer">
                <div>Features</div>
                <div>Pricing</div>
                <div>Integrations</div>
              </div>
            </div>
            <div class="col-6 col-md-2">
              <div class="text-subtitle1 text-weight-bold q-mb-sm">Support</div>
              <div class="text-grey-5 column q-gutter-ys-sm cursor-pointer">
                <div>Help Center</div>
                <div>API Documentation</div>
                <div>Contact Us</div>
              </div>
            </div>
            <div class="col-12 col-md-4">
              <div class="text-subtitle1 text-weight-bold q-mb-sm">Subscribe</div>
              <p class="text-grey-5">Join our newsletter for the latest updates.</p>
              <q-input dark dense outlined placeholder="Enter email" class="q-mb-sm">
                <template v-slot:append>
                  <q-btn round dense flat icon="send" color="primary" />
                </template>
              </q-input>
            </div>
          </div>
          <div class="row justify-between items-center q-mt-xl text-grey-6 text-caption">
            <div>© 2024 Customer Management System. All rights reserved.</div>
            <div class="q-gutter-sm">
              <q-icon name="facebook" size="20px" class="cursor-pointer hover-red" />
              <q-icon name="ion-logo-twitter" size="20px" class="cursor-pointer hover-red" />
              <q-icon name="ion-logo-linkedin" size="20px" class="cursor-pointer hover-red" />
            </div>
          </div>
        </div>
      </footer>
    </q-page-container>
  </q-layout>
</template>

<script setup>
// Main Layout Logic

function scrollToSection(id) {
  const element = document.getElementById(id)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth', block: 'start' })
  }
}
</script>

<style lang="scss">
.hover-red {
  transition: color 0.3s;
  &:hover {
    color: $primary;
  }
}

/* Navigation Button Effects */
.nav-btn {
  position: relative;
  transition: color 0.3s ease;
  overflow: visible;

  &::after {
    content: '';
    position: absolute;
    bottom: 5px; /* Sits just inside the button area */
    left: 0;
    width: 100%;
    height: 2px;
    background-color: $primary;
    transform: scaleX(0);
    transform-origin: center;
    transition: transform 0.3s ease;
  }

  &:hover {
    color: $primary !important;

    &::after {
      transform: scaleX(1);
    }
  }

  /* Hide Quasar's default ripple/focus to keep it clean */
  .q-focus-helper {
    display: none !important;
  }
}

.scale-hover {
  transition:
    transform 0.3s ease,
    box-shadow 0.3s ease;

  &:hover {
    transform: scale(1.05);
    box-shadow: 0 4px 15px rgba(213, 0, 0, 0.4);
  }
}

.nav-btn-outline {
  transition:
    background-color 0.3s,
    color 0.3s;

  &:hover {
    background-color: $primary !important;
    color: white !important;
  }
}

body {
  overflow-x: hidden;
}
</style>
