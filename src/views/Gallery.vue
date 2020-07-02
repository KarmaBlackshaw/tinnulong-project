<template>
  <v-sheet
    id="gallery"
    color="#333333"
    dark
    tag="section"
    tile
  >
    <div class="py-12" />

    <v-container>
      <h2 class="display-2 font-weight-bold mb-3 text-uppercase text-center">
        Gallery
      </h2>

      <v-responsive
        class="mx-auto mb-12"
        width="56"
      >
        <v-divider class="mb-1" />

        <v-divider />
      </v-responsive>

      <v-theme-provider light>
        <v-row>
          <v-col
            cols="12"
          >
            <v-card>
              <v-container fluid>
                <v-row>
                  <v-col
                    v-for="n in 20"
                    :key="n"
                    class="d-flex child-flex"
                    cols="4"
                  >
                    <v-card
                      flat
                      tile
                      class="d-flex"
                    >
                      <v-img
                        :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                        :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                        aspect-ratio="1"
                        class="grey lighten-2"
                      >
                        <template v-slot:placeholder>
                          <v-row
                            class="fill-height ma-0"
                            align="center"
                            justify="center"
                          >
                            <v-progress-circular
                              indeterminate
                              color="grey lighten-5"
                            />
                          </v-row>
                        </template>
                      </v-img>
                    </v-card>
                  </v-col>
                </v-row>
              </v-container>
            </v-card>
          </v-col>
        </v-row>
      </v-theme-provider>
    </v-container>

    <div class="py-12" />
  </v-sheet>
</template>

<script>
export default {

}
</script>

<style>

</style>
