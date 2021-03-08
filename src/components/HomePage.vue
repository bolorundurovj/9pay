<template>
  <v-container>
    <!-- <v-row>
      <v-col cols="12">
        <v-input
          append-icon="mdi-close"
          prepend-icon="mdi-magnify"
          label="Search Here"
        >
        </v-input>
      </v-col>
    </v-row> -->
    <v-layout row wrap class="mt-4">
      <v-flex xs12>
        <v-carousel style="cursor: pointer">
          <v-carousel-item
            v-for="slide in slides"
            :key="slide"
            :src="slide"
            reverse-transition="fade-transition"
            transition="fade-transition"
          >
          </v-carousel-item>
        </v-carousel>
      </v-flex>
    </v-layout>
    <div
      class="container my-12 mx-auto px-4 md:px-12"
      v-for="merchant in merchants"
      :key="merchant"
    >
      <div class="text-xl font-bold">{{ merchant.name }}</div>
      <div class="flex flex-wrap -mx-1 lg:-mx-4">
        <div
          class="my-1 px-1 w-full md:w-1/3 lg:my-4 lg:px-4 lg:w-1/4"
          v-for="product in merchant.products"
          :key="product"
        >
          <article class="overflow-hidden rounded-lg shadow-lg">
            <a href="/">
              <img
                alt="Placeholder Image"
                class="block h-auto w-full"
                src="https://picsum.photos/600/400/?random"
              />
            </a>

            <header
              class="flex items-center justify-center leading-tight p-2 md:p-4"
            >
              <h1 class="text-lg text-center">
                <a
                  class="no-underline hover:underline text-grey-700"
                  style="color: black"
                  href="#"
                >
                  {{ product }}
                </a>
              </h1>
            </header>
          </article>
        </div>
      </div>
    </div>
  </v-container>
</template>

<script>
export default {
  name: "HomePage",
  computed: {
    slides() {
      return [
        "https://images.pexels.com/photos/1447092/pexels-photo-1447092.png?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
        "https://images.pexels.com/photos/132037/pexels-photo-132037.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260",
        "https://images.pexels.com/photos/747964/pexels-photo-747964.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260",
      ];
    },
    merchants() {
      return [
        {
          name: "Product Merchants",
          products: [
            "Product 1",
            "Product 2",
            "Product 3",
            "Product 4",
            "Product 5",
            "Product 6",
            "Product 7",
            "Product 8",
            "Product 9",
            "Product 10",
            "Product 11",
            "Product 12",
          ],
        },
        {
          name: "Service Merchants",
          products: [
            "Service 1",
            "Service 2",
            "Service 3",
            "Service 4",
            "Service 5",
            "Service 6",
            "Service 7",
            "Service 8",
            "Service 9",
            "Service 10",
            "Service 11",
            "Service 12",
          ],
        },
      ];
    },
  },
};
</script>
