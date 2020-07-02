<template>
  <section
    id="features"
    class="grey lighten-3"
  >
    <div class="py-12" />

    <v-container class="text-center">
      <h2 class="display-1 font-weight-bold mb-3">
        GET INVOLVED IN OUR INNOVATION
      </h2>

      <v-responsive
        class="mx-auto mb-12"
        width="56"
      >
        <v-divider class="mb-1" />

        <v-divider />
      </v-responsive>

      <v-row>
        <v-col
          v-for="({ icon, title, text, color }, i) in features"
          :key="i"
          cols="12"
          md="6"
        >
          <v-card
            class="py-12 px-4"
            color="grey lighten-5"
            elevation="2"
            height="400"
          >
            <v-theme-provider dark>
              <div>
                <v-avatar
                  :color="color"
                  size="90"
                >
                  <v-icon
                    large
                    v-text="icon"
                  />
                </v-avatar>
              </div>
            </v-theme-provider>

            <v-card-title
              class="justify-center font-weight-black text-uppercase"
              v-text="title"
            />

            <v-card-text
              class="subtitle-1"
              v-text="text"
            />
          </v-card>
        </v-col>
      </v-row>
    </v-container>

    <div class="py-12" />
  </section>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',

  data: () => ({
    features: [
      {
        icon: 'mdi-account-group-outline',
        color: 'green',
        title: 'Volunteer Opportunities',
        text: 'There are many ways for you to contribute to our charitable endeavours, one of which is to get involved with some of our important causes. Believe us when we say that every little bit of help is appreciated and counts, especially for those in need. Read on to learn more about what we do and how you can lend your support.'
      },
      {
        icon: 'mdi-elevation-rise',
        color: 'orange',
        title: 'Fundraising Opportunities',
        text: 'The human nature of giving is one of the most powerful forces. At TINNULONG FOUNDATION, INC, we harness the efforts of our staff and volunteers to positively impact the lives of those most in need of assistance. We’d love for you to join us in helping to improve the situations of people in need from the Bacnotan community.'
      },
      {
        icon: 'mdi-food-apple',
        color: 'red',
        title: 'Feeding Children',
        text: 'One of our main causes here at TINNULONG FOUNDATION, INC is Feeding Children, an issue that touches many lives, particularly those in the greater Bacnotan area. We spend a significant portion of our resources on tackling this problem.'
      },
      {
        icon: 'mdi-home-lightbulb',
        color: 'blue',
        title: 'Housing the Homeless',
        text: 'One of the main reasons TINNULONG FOUNDATION, INC was founded in 2000 was to compensate for the greater Bacnotan area’s struggles with Housing the Homeless. We’ve dedicated a lot of man-hours and invested countless resources to this charitable cause, and hope you’ll help us continue this work.'
      }
    ]
  })
}
</script>
