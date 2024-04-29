<template>
  <div>
    <div>
             <v-card>
               <v-img
                 :aspect-ratio="16 / 9"
                 dark
                 gradient="to top, rgba(25,32,72,.7), rgba(25,32,72,.0)"
                 height="500px"
                 src="https://images.pexels.com/photos/3244513/pexels-photo-3244513.jpeg"
               >
                 <v-card-text class="fill-height d-flex align-end">
                   <v-row class="flex-column">
                     <v-col>
                       <v-btn color="accent" to="category">Explore</v-btn>
                     </v-col>
                     <v-col cols="12" lg="8" md="10" xl="7">
                       <h2 class="text-h3 py-3" style="line-height: 1.2">
                        Great places Around the World To Inspire You
                       </h2>
                     </v-col>
                     <v-col class="d-flex align-center">
                       <v-avatar class="elevation-4" color="accent"></v-avatar>
                     </v-col>
                   </v-row>
                 </v-card-text>
               </v-img>
             </v-card>
           </div>
 
     <v-row>
       <v-col cols="12" lg="12" xl="8">
         <div>
           <div class="pt-16">
             <h2 class="text-h4 font-weight-bold pb-4">Recommended places you can visit</h2>
 
             <v-row>
               <v-col v-for="(place, index) in places" :key="index" cols="12" lg="4" md="6">
                 <v-hover
                  v-slot:default="{ hover }"
                  close-delay="50"
                  open-delay="50"
                 >
                  <div>
                     <v-card
                       :color="hover ? 'white' : 'transparent'"
                       :elevation="hover ? 12 : 0"
                       flat
                       hover
                     >
                       <v-img
                         :aspect-ratio="16 / 9"
                         class="elevation-2"
                         gradient="to top, rgba(25,32,72,.4), rgba(25,32,72,.0)"
                         height="200px"
                         :src="place.image"
                         style="border-radius: 16px"
                       >
                         <v-card-text></v-card-text>
                       </v-img>
 
                       <v-card-text>
                         <div class="text-h5 font-weight-bold primary--text">
                           {{ place.name }}
                         </div>
 
                         <div class="text-body-1 py-4">
                           {{ place.description }}
                         </div>
 
                         <div class="d-flex align-center">
                           <v-avatar color="accent" size="36">
                             <v-icon dark>mdi-feather</v-icon>
                           </v-avatar>
 
                           <div class="pl-2"></div>
                           <div class="pl-2">Location:Cape Town</div>
                         </div>
                       </v-card-text>
                     </v-card>
                  </div>
                 </v-hover>
               </v-col>
             </v-row>
           </div>
         </div>
       </v-col>
 
       <v-col>
         <div class="pt-16">
           <siderbar/>
         </div>
       </v-col>
     </v-row>
  </div>
 </template>
 
 <script>
 export default {
  name: "Home",
  components: {
     siderbar: () => import("@/components/details/sidebar"),
  },
  data() {
     return {
       places: [
         {
           name: "Clifton",
           image: "/images/clifton.jpg",
             
         },
         {
           name: "Waterfront",
           image: "/images/V&A.jpeg",
           
         },
         {
           name: "Kenilworth",
           image: "/images/Parklands.jpg",
           
         }
         
       ]
     };
  }
 };
 </script>
 