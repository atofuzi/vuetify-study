<template>
 <v-container style="height: 1500px;">
    <v-row justify="center">
      <v-col
        v-for="n in 10"
        :key="n"
        cols="auto"
      >
        <v-card
          :elevation="n - 1"
          height="100"
          width="100"
          color="pink"
        >
          <v-row
            class="fill-height"
            align="center"
            justify="center"
            v-text="n - 1"
          ></v-row>
        </v-card>
      </v-col>
    </v-row>
  <div class="text-center">
    <div class="test">test</div>
    <v-slider
      v-model="model"
      :max="rounded.length - 1"
      :tick-labels="rounded"
    ></v-slider>

    <div class="py-3"></div>

    <v-sheet
      :class="radius"
      :max-width="model === 6 ? 128 : 256"
      class="mx-auto transition-swing"
      elevation="12"
      height="128"
      width="100%"
      color="green lighten-3"
    ></v-sheet>

    <div class="py-3"></div>

    <code class="text-subtitle-1">.{{ radius }}</code>
    <blockquote class="blockquote" cite="https://www.huxley.net/bnw/four.html">
        <p>Words can be like X-rays, if you use them properly—they’ll go through anything. You read and you’re pierced.</p>
    </blockquote>
  </div>
    <v-sheet
    :min-height="$vuetify.breakpoint.xs ? 300 : '20vh'"
    :rounded="$vuetify.breakpoint.xsOnly"
    color="red"
  >
    ...
  </v-sheet>
    </v-container>

</template>
<script>

  export default {
    data: () => ({
      model: 3,
      rounded: [
        '0',
        'sm',
        'md',
        'lg',
        'xl',
        'pill',
        'circle',
      ],
    }),

    computed: {
      radius () {
        let rounded = 'rounded'
        const value = this.rounded[this.model]

        if (value !== 'md') {
          rounded += `-${value}`
        }
        console.log(this.rounded.length)
        return rounded
      },
    },
  }
</script>