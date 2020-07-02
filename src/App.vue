<template>
  <div id="app">
    <v-app>
      <navbar />

      <v-content>
        <home-section />
        <features-section />
        <gallery-section />
        <about-section />

        <section id="stats">
          <v-parallax
            :height="$vuetify.breakpoint.smAndDown ? 700 : 500"
            :src="require('@/assets/stats_1.jpg')"
          >
            <v-container fill-height>
              <v-row class="mx-auto">
                <v-col
                  v-for="[value, title] of stats"
                  :key="title"
                  cols="12"
                  md="3"
                >
                  <div class="text-center">
                    <div
                      class="display-3 font-weight-black mb-4"
                      v-text="value"
                    />

                    <div
                      class="title font-weight-regular text-uppercase"
                      v-text="title"
                    />
                  </div>
                </v-col>
              </v-row>
            </v-container>
          </v-parallax>
        </section>

        <blog-section />

        <contact-section />
      </v-content>

      <v-footer
        class="justify-center"
        color="#292929"
        height="100"
      >
        <div class="title font-weight-light grey--text text--lighten-1 text-center">
          &copy; {{ (new Date()).getFullYear() }} — Tinnulong Foundation Inc.
        </div>
      </v-footer>
    </v-app>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
import HomeSection from '@/views/Home'
import AboutSection from '@/views/About'
import FeaturesSection from '@/views/Features'
import ContactSection from '@/views/Contact'
import GallerySection from '@/views/Gallery'
import BlogSection from '@/views/Blog'

export default {
  name: 'App',

  components: {
    Navbar,
    HomeSection,
    AboutSection,
    FeaturesSection,
    ContactSection,
    GallerySection,
    BlogSection
  },

  data: () => ({
    stats: [
      ['24k', 'Families'],
      ['330+', 'Children'],
      ['1m', 'Supporters'],
      ['5m', 'Total Contributors']
    ]
  })
}
</script>
