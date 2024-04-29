<template>
  <div>
    <v-card absolute app color="primary" dark flat>
      <v-container>
        <v-row align="start">
         

          <v-col cols="12" md="3">
            <v-list color="transparent" flat>
              <v-subheader class="text-h6"></v-subheader>
              <v-list-item-group color="primary">
                <v-list-item
                    v-for="(item, i) in heroui"
                    :key="i"
                    :href="item.href"
                    dense
                    target="_black"
                >
                  <v-list-item-content>
                    <v-list-item-title
                        class="text-body-1"
                        v-text="item.text"
                    ></v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list-item-group>
            </v-list>
          </v-col>

          <v-col cols="12" md="3">
            <v-list color="transparent" flat>
              <v-subheader class="text-h6">Contact us</v-subheader>
              <v-list-item-group color="primary">
                <v-list-item
                    v-for="(item, i) in shock"
                    :key="i"
                    :href="item.href"
                    dense
                    target="_black"
                >
                  <v-list-item-content>
                    <v-list-item-title
                        class="text-body-1"
                        v-text="item.text"
                    ></v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list-item-group>
            </v-list>
          </v-col>

          <v-col cols="12" md="3">
            <div>
              <h5 class="text-h6 font-weight-bold">
                FOLLOW US
              </h5>
              <p class="text-body-1">
 <v-btn icon href="https://www.facebook.com" target="_blank">
    <v-icon>mdi-facebook</v-icon>
    FACEBOOK
 </v-btn>
</p>

              <p class="text-body-1">
 <v-btn icon href="https://www.twitter.com" target="_blank">
    <v-icon>mdi-twitter</v-icon>
    TWITTER
 </v-btn>
</p>

              <p class="text-body-1">
 <v-btn icon href="https://www.instagram.com" target="_blank">
    <v-icon>mdi-instagram</v-icon>
    INSTAGRAM
 </v-btn>
</p>

              <p class="text-body-1">
 <v-btn icon href="https://www.youtube.com" target="_blank">
    <v-icon>mdi-youtube</v-icon>
    YOUTUBE
 </v-btn>
</p>

            </div>

            <v-row>
            

             
            </v-row>
          </v-col>
        </v-row>

        <div class="text-center mt-6">
          Copyright &copy;
          <a
              class="white--text"
              href="https://heroui.net"
              rel="noopener noreferrer"
              target="_blank"
          >WE TRAVEL</a
          >
          {{ new Date().getFullYear() }}. All rights reserved.
        </div>
      </v-container>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    shock: [
      {
        text: "Facebook",
        href: "https://heroui.net/",
      },
      {
        text: "Linkedin",
        href: "https://heroui.net/",
      },
      {
        text: "Instagram",
        href: "https://heroui.net/",
      },
    ],
    shock: [
      {
        text: "+21633135682",
        
      },
      {
        text: "wetravel@gmail.com",
       
      },
      {
        text: "www.wetravel.co.za",
  
      },
    ],
  }),
};
</script>
