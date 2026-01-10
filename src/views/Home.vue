<script setup lang="ts">

import CardComponent from '../components/CardComponent.vue';
import BadgeComponent from '../components/BadgeComponent.vue';
import TitleComponent from '../components/TitleComponent.vue';


</script>

<template> 
  <div class="flex justify-center">
    <CardComponent class="max-w-md mt-4 mb-4 mx-0 w-full">
      <template #header>
        <div class="flex justify-between items-center"> 
            <TitleComponent title="Web Developer" />
         
          <BadgeComponent additional_class="active" msg="Looking for work" />
        </div>
      </template> 

      <div class="flex gap-2 items-center">
        <div class="w-2/3">
          <h2 class="text-xl font-semibold mb-4">I'm Joseph Rivera Jr</h2>
          <p class="text-sm mt-2 text-gray-500"><b>5+ years of experience</b> building with modern JavaScript frameworks, emphasizing <b>UI/UX, performance, and scalability.</b></p>
        </div>
        <div class="flex justify-end w-1/3">
          <img src="/src/assets/images/profile.webp" alt="Logo" class="w-32 h-32 profile-pic" />
        </div>

      </div>
      
      <div class="mt-5">
        <div class="flex">
            <TitleComponent title="Skills" />
        </div> 
            <CardComponent class="max-w-md mt-2 mx-0 w-full">
              <div class="flex gap-2 justify-between items-center">
              <p>Core Web Technologies</p>
                <img src="https://cdn-icons-png.flaticon.com/512/136/136528.png" alt="HTML" class="w-8 h-8">
                <img src="https://cdn-icons-png.flaticon.com/512/136/136527.png" alt="CSS" class="w-8 h-8">
                <img src="https://cdn-icons-png.flaticon.com/512/136/136530.png" alt="JS" class="w-8 h-8">
              </div>
            </CardComponent>
            <CardComponent class="max-w-md mt-2 mx-0 w-full">
              <div class="flex gap-2 justify-between items-center">
              <p>JavaScript Frameworks</p>
                <img src="https://images.seeklogo.com/logo-png/27/1/vue-js-logo-png_seeklogo-274070.png" alt="VUE" class="w-8 h-8">
                <img src="https://img.icons8.com/color/256/react-native.png" alt="REACT" class="w-8 h-8">
                <img src="https://cdn-icons-png.flaticon.com/512/5968/5968322.png" alt="NODEJS" class="w-8 h-8">
              </div>
            </CardComponent>

            <CardComponent class="max-w-md mt-2 mx-0 w-full">
              <div class="flex gap-2  justify-between items-center">
              <p>UI Frameworks & Libraries</p>
                <img src="https://cdn-icons-png.flaticon.com/512/5968/5968672.png" alt="Bootstrap" class="w-8 h-8"> 
                <img src="https://code.dlang.org/packages/tailwind-d/logo?s=650228a573eaa51f8ceded68" alt="Tailwind" class="w-8 h-8"> 
                <img src="https://img.icons8.com/color/452/material-ui.png" alt="Material UI" class="w-8 h-8"> 
              
              </div>
            </CardComponent>

            <CardComponent class="max-w-md mt-2 mx-0 w-full">
              <div class="flex gap-2 items-center ">
              <p>Backend Frameworks</p>
                <img src="https://cdn-icons-png.flaticon.com/512/6785/6785635.png" alt="Laravel" class="w-8 h-8 ml-4"> 
                Laravel
              </div>
            </CardComponent>

            <CardComponent class="max-w-md mt-2 mx-0 w-full">
              <div class="flex gap-2  justify-between items-center">
              <p>Data and Integration</p>
                <img src="https://upload.wikimedia.org/wikipedia/commons/9/96/Socket-io.svg" alt="socket.io" class="w-8 h-8"> 
                <img src="https://1.bp.blogspot.com/-Ar8WR3ySYG8/WAuTyMYRNcI/AAAAAAAAO9M/PJOWp3Z8iGUly911EjMP0JjLgfi3EaiLwCLcB/s1600/REST%2BAPI.png" alt="Restfult API" class="w-8 h-8"> 
                <img src="https://dn721902.ca.archive.org/0/items/github.com-axios-axios_-_2021-05-07_16-44-30/cover.jpg" alt="Axios" class="w-8 h-8"> 
              
              </div>
            </CardComponent>
            

      </div>

      
      <div class="mt-5">
        <div class="flex items-start gap-2">
            <TitleComponent title="Projects" />
        </div> 
            <b class="block mt-4">Personal Projects</b>
            <CardComponent class="max-w-md mt-2 mx-0 w-full"> 
              <p>POS - Orange and Cafe</p> 
              <p class="text-right">
                <router-link class="text-blue-400 " to="/project/orangeCafe"><span >View more</span></router-link> 
              </p> 
            </CardComponent>  
            <CardComponent class="max-w-md mt-2 mx-0 w-full">  
              <p clas>Budget Plan</p>
              <!-- <p>Link: <a class="text-blue-400" target="_blank" href="https://budgetplan-sheesh.surge.sh/">https://budgetplan-sheesh.surge.sh/</a></p>  -->
              <p class="text-right">
                <router-link class="text-blue-400 " to="/project/budget"><span >View more</span></router-link> 
              </p> 
            </CardComponent> 

            <b class="block mt-4">Career Projects</b>
            <CardComponent class="max-w-md mt-2 mx-0 w-full">  
              <p>Robinsons Supermarket</p>
              <!-- <p>Link: <a class="text-blue-400" style="overflow-wrap: break-word;" target="_blank" href="https://www.robinsonssupermarket.com.ph/">https://www.robinsonssupermarket.com.ph/</a></p>  -->

              <p class="text-right">
                <router-link class="text-blue-400 " to="/project/Robinson"><span >View more</span></router-link> 
              </p> 
            </CardComponent> 

            <!-- <CardComponent class="max-w-md mt-2 mx-0 w-full"> 
              <p>Bingo Pilipino</p>
              <p>Link: <a class="text-blue-400" target="_blank" href="http://staging.bingopilipino.com/q9f2kpz7mfjxA3yLwB8nght4">http://staging.bingopilipino.com/</a></p> 
            </CardComponent>  -->

            <CardComponent class="max-w-md mt-2 mx-0 w-full"> 
              <p>Daily by Bo's Coffee</p> 

              <p class="text-right">
                <router-link class="text-blue-400 " to="/project/dailys"><span >View more</span></router-link> 
              </p> 
            </CardComponent> 

            <CardComponent class="max-w-md mt-2 mx-0 w-full"> 
              <p>Zagana</p>
              
              <p class="text-right">
                <router-link class="text-blue-400 " to="/project/zagana"><span >View more</span></router-link> 
              </p> 
            </CardComponent>  

      </div>

      <template #footer>
        <!-- <button class="mt-3 px-4 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-700">
          View Details
        </button> -->
        <p class="text-3xl mt-4">Let's work together!</p>
        <p>For more details about my experience and projects, feel free to <a class="text-blue-400" target="_blank" href="https://www.canva.com/design/DAFcZWtXfmc/IZH8xgzs0x7xkRrIc8XAqw/view#1">download or view my resume</a>.</p>
        <p>or feel free to email me at <a class="text-blue-400" target="_blank" href="sephriverajr@gmail.com">sephriverajr@gmail.com</a>.</p>
      </template>
    </CardComponent> 
  </div>
</template>

<style scoped>
  .profile-pic {
    border-radius: 50%;
    box-shadow: rgb(236, 239, 244) 0px 0px 0px 2.22222px;
  }
</style>
