<template>
  <div>
     <v-row>
       <v-col cols="12" lg="12" xl="8">
         <div>
           <v-card flat color="transparent">
             <v-img
               src="/images/clifton.jpg"
               :aspect-ratio="16 / 9"
               gradient="to top, rgba(25,32,72,.4), rgba(25,32,72,.0)"
               style="border-radius: 16px"
             ></v-img>
 
             <v-card-text>
              
 
               <div class="text-h4 font-weight-bold primary--text pt-4">
                 <h4>CLIFTON</h4>
               </div>
 
               <div class="text-body-1 py-4">
                 Location: CAPE TOWN.
               </div>
 
               <div class="d-flex align-center justify-space-between">
                 <div class="d-flex align-center">
                  <v-avatar color="accent" size="36">
                     <v-icon dark>mdi-feather</v-icon>
                  </v-avatar>
 
                  <div class="pl-2 text-body-1">OPEN HOURS: 9AM-9PM</div>
                 </div>
 
                 <div class="d-flex align-center">
                  <div>
                     <v-chip small color="transparent">
                       <v-icon left>mdi-eye</v-icon>
                     </v-chip>
                  </div>
                 </div>
               </div>
 
               <v-divider class="my-4"></v-divider>
 
               <div>
                 <p class="text-subtitle-1 primary--text font-weight-medium">
                  Clifton is a seaside neighborhood in Cape Town, known for its luxurious lifestyle and being a playground for the rich. It is renowned for its beautiful beaches, stunning views, and high-end properties, making it a desirable location for those seeking a luxurious lifestyle. The area is characterized by its affluent residents and is often referred to as a "playground for the rich," highlighting its exclusivity and the high value of properties within the neighborhood
                  
                 </p>
               </div>
 
               <div class="d-flex align-center justify-space-between mt-8">
                
               </div>
             </v-card-text>
           </v-card>
         </div>
       </v-col>
 
       <v-col>
         <div>
           <siderbar />
         </div>
       </v-col>
     </v-row>
  </div>
 </template>
 

<script>
export default {
  name: "Category",
  components: {
    siderbar: () => import("@/components/details/sidebar")
  }
};
</script>
