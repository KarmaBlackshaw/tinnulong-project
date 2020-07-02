<template>
  <v-sheet
    id="contact"
    color="#333333"
    dark
    tag="section"
    tile
  >
    <div class="py-12" />

    <v-container>
      <h2 class="display-2 font-weight-bold mb-3 text-uppercase text-center">
        Contact Me
      </h2>

      <v-responsive
        class="mx-auto mb-12"
        width="56"
      >
        <v-divider class="mb-1" />

        <v-divider />
      </v-responsive>

      <v-theme-provider light>
        <v-row dense>
          <v-col
            cols="12"
            md="6"
            sm="12"
          >
            <v-col cols="12">
              <v-text-field
                flat
                label="Name*"
                hide-details
                solo
              />
            </v-col>

            <v-col cols="12">
              <v-text-field
                flat
                label="Email*"
                hide-details
                solo
              />
            </v-col>

            <v-col cols="12">
              <v-text-field
                flat
                label="Subject*"
                hide-details
                solo
              />
            </v-col>

            <v-col cols="12">
              <v-textarea
                flat
                label="Message*"
                hide-details
                solo
              />
            </v-col>

            <v-col
              class="mx-auto"
              cols="auto"
            >
              <v-btn
                color="accent"
                x-large
              >
                Submit
              </v-btn>
            </v-col>
          </v-col>

          <v-col
            cols="12"
            md="6"
            sm="12"
          >
            <v-container>
              <v-card>
                <v-list flat>
                  <v-list-item-group color="primary">
                    <v-list-item
                      v-for="(contactItem, contactKey) in contactInformation"
                      :key="contactKey"
                    >
                      <v-list-item-icon v-if="contactItem.icon">
                        <v-icon v-text="contactItem.icon" />
                      </v-list-item-icon>
                      <v-list-item-action v-else />

                      <v-list-item-content>
                        <v-list-item-title v-text="contactItem.text" />
                        <template v-if="contactItem.subtitle">
                          <v-list-item-subtitle
                            v-for="(subItem, subKey) in contactItem.subtitle"
                            :key="subKey"
                            v-text="subItem"
                          />
                        </template>
                      </v-list-item-content>
                    </v-list-item>
                  </v-list-item-group>
                </v-list>
              </v-card>
            </v-container>
          </v-col>
        </v-row>
      </v-theme-provider>
    </v-container>

    <div class="py-12" />
  </v-sheet>
</template>

<script>
export default {
  data: () => ({
    social: {
      facebook: 'https://www.facebook.com/Tinnulong-Foundation-Inc-1538391719521216'
    },
    contactInformation: [
      {
        icon: 'mdi-map-marker',
        text: 'MacArthur Highway, Bacnotan, La Union, Philippines'
      },
      {
        icon: 'mdi-email',
        text: 'jhonel.santiago@yahoo.com'
      },
      {
        icon: 'mdi-phone',
        text: 'Mr. Ignacio',
        subtitle: ['+63 917 5405 080']
      },
      {
        text: 'Ms. Leah',
        subtitle: ['+63 995 0461 118']
      },
      {
        text: 'Mr. Jonel',
        subtitle: ['+63 915 2793 379', '+63 920 6511 174']
      }
    ]
  })
}
</script>

<style>
</style>
