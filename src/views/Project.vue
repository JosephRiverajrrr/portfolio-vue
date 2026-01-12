<script setup lang="ts">
import { useRoute } from 'vue-router'
import CardComponent from '../components/CardComponent.vue'; 
import TitleComponent from '../components/TitleComponent.vue';

const route = useRoute()
const projectUrl = route.params.url as string;

const projects = [
    {   slug: 'orangeCafe',
        title: 'POS - Orange Cafe',
        description: ['Built a web-based POS system using Vue.js and Firebase with real-time transaction processing.',
            'Implemented inventory management with automatic stock updates after each sale.',
            'Generated sales summary reports to track business performance and revenue trends'
        ],
        stack: [
            '/images/vue.png',
            '/images/firebase.png'
        ],
        images: [ 
             '/images/orangeCafe/orangeCafe1.png'
        ]
    },
    {   slug: 'budget',
        title: 'Budget Plan',
        description: ['A personal project designed to track expenses and savings.',
            'Records monthly expenses and allows users to set a Target Savings Amount.',
            'Includes expense history tracking.',
            'Built from scratch using: ReactJS, Firebase, MUI.'
        ],
        stack: [
            '/images/react.png',
            '/images/firebase.png',
            '/images/materialui.png'
        ],
        images: [ 
           '/images/budget/budget1.png'
        ]
    },

    {
        slug: 'Robinson',
        title: 'Robinsons Supermarket',
        description: ['Built a dynamic CMS allowing admins to manage news, promos, and product listings (CRUD) using a Laravel–MySQL backend',
            'Implemented responsive frontend components using HTML, CSS, JavaScript, jQuery, and Bootstrap, consuming dynamic data from the backend.',
            'Developed a user-facing website with a clean, responsive UI for browsing products, promotions, and announcements across mobile and desktop.',
            'Integrated Google Analytics for traffic and engagement tracking and Google Maps API to display and locate physical store branches.'
        ],
        stack: [
            'https://cdn-icons-png.flaticon.com/512/136/136528.png',
            'https://cdn-icons-png.flaticon.com/512/136/136527.png',
            'https://cdn-icons-png.flaticon.com/512/136/136530.png',
            '/images/bootstrap.png',
            '/images/php.png'
        ],
        images: [ 
             '/images/Robinson/Robinson1.png'
        ]
    },

    {
        slug: 'zagana',
        title: 'Zagana',
        description: ['Built a produce e-commerce platform with a customer-facing storefront and an admin/backoffice dashboard for managing products, inventory, and content.',
            'Developed responsive UIs using ReactJS with Bootstrap (storefront) and Material UI (MUI) (admin panel), styled with Sass/SCSS',
            'Implemented Node.js RESTful APIs and MySQL database schemas for users, products, orders, and transactions.',
            'Focused on performance, usability, and a seamless experience for both buyers and administrators.'
        ],
        stack: [
            '/images/react.png',
            '/images/nodejs.png',
            '/images/bootstrap.png',
            '/images/restfulapi.png'
        ],
        images: [ 
             '/images/zagana/zagana1.png'
        ]
    },

    {
        slug: 'dailys',
        title: "Daily by Bo's Coffee",
        description: ['Built a produce e-commerce platform with a customer-facing storefront and an admin/backoffice dashboard for managing products, inventory, and content.',
            'Developed responsive UIs using ReactJS with Bootstrap (storefront) and Material UI (MUI) (admin panel), styled with Sass/SCSS',
            'Implemented Node.js RESTful APIs and MySQL database schemas for users, products, orders, and transactions.',
            'Focused on performance, usability, and a seamless experience for both buyers and administrators.'
        ],
        stack: [
            '/images/react.png',
            '/images/nodejs.png',
            '/images/bootstrap.png',
            '/images/restfulapi.png'
        ],
        images: [ 
             '/images/dailys/dailys2.png'

        ]
    }
 

]

const project = projects.find(
  (p) => p.slug === projectUrl
)


</script>

<template>  
  <div v-if="project" class="flex justify-center">
    <CardComponent class="max-w-md mt-4 mb-4 mx-0 w-full">
        
      <template #header>
        <div class="flex gap-2 items-center"> 

        <div class="flex justify-center items-center pointer">
            <router-link class="text-blue-400 " to="/"> <img  class="w-4 h-4" src="https://www.svgrepo.com/show/535197/arrow-u-up-left.svg" /></router-link> 
           
        </div>
        <h2 class="text-3xl">{{ project.title }}</h2>
          
        </div>
      </template> 
      <div class="my-5">   
        <div class="flex justify-center items-start gap-2">      
            <CardComponent class="max-w-md mt-2 mx-0 w-full">
              <div>    
                        <img 
                        v-for="(img, i) in project.images"
                        :key="i"
                        :src="img"
                        :alt="img"
                    />
              </div>
            </CardComponent> 
        </div>  

      </div>

      <div class=" items-center"> 
             <ul>
                <li v-for="(item, i) in project.description" :key="i">
                    &#9679;	 {{ item }}
                </li>
            </ul> 
       

      </div>
      
      <div class="mt-5">
        <div class="flex">
        </div> 
            <TitleComponent title="Tech Stack" />
            <CardComponent class="max-w-md mt-2 mx-0 w-full">
              <div class="flex gap-4 justify-center items-center">   
                        <img
                        class="w-12 h-12"
                        v-for="(img, i) in project.stack"
                        :key="i"
                        :src="img"
                        :alt="'.'+img"
                    />
              </div>
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

  <p v-else>Project not found</p>
</template>
