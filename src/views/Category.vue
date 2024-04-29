<template>
  <div>
     <div>
       <h2 class="text-h4 font-weight-bold">LIST OF PLACES AROUND YOU</h2>
     </div>
     <v-divider class="my-4"></v-divider>
     <v-row>
       <v-col cols="12" md="6" lg="4" v-for="(place, index) in places" :key="index">
         <v-hover
           v-slot:default="{ hover }"
           open-delay="50"
           close-delay="50"
         >
           <div>
             <v-card
               flat
               :color="hover ? 'white' : 'transparent'"
               :elevation="hover ? 12 : 0"
               hover
               to="/detail"
             >
               <v-img
                 :src="place.image"
                 :aspect-ratio="16 / 9"
                 gradient="to top, rgba(25,32,72,.4), rgba(25,32,72,.0)"
                 height="200px"
                 class="elevation-2"
                 style="border-radius: 16px"
               >
                 <v-card-text>
                  <v-btn color="accent">VIEW MORE DETAILS</v-btn>
                 </v-card-text>
               </v-img>
 
               <v-card-text>
                 <div class="text-h5 font-weight-bold primary--text">
                  {{ place.text }}
                 </div>
 
                
 
                 <div class="d-flex align-center">
                  <v-avatar color="accent" size="36">
                     <v-icon dark>mdi-feather</v-icon>
                  </v-avatar>
 
                  <div class="pl-2">Location : Cape Town</div>
                 </div>
               </v-card-text>
             </v-card>
           </div>
         </v-hover>
       </v-col>
     </v-row>
  </div>
 </template>
 



      
          
  
                
             
    
  
  <script>
  export default {
   name: "Category",
   components: {
      siderbar: () => import("@/components/details/sidebar"),
   },
   data() {
 return {
    places: [
      { image: '/images/clifton.jpg', text: 'Clifton' },
      { image: '/images/Muizenberg.jpeg', text: 'Muizenberg' },
      { image: '/images/table-mountain.jpg', text: 'Table Mountain' },
      { image: '/images/V&A.jpeg', text: 'V&A Waterfront' },
      { image: '/images/Grand West.jpg', text: 'Grand West' },
      { image: '/images/Kenilworth.jpg', text: 'Kenelworth' },
    ]
 };
}

  };
  </script>
  

