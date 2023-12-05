<script setup>
import { faker } from '@faker-js/faker'

const firstName = faker.name.firstName()
const lastName = faker.name.lastName()
const fullName = `${ firstName } ${ lastName }`

const selectCard = () => {
    console.log(`${fullName} selected`)
}
</script>

<template>
    <div class="card" @click="selectCard">
        <div class="card-image">
            <img :src="faker.internet.avatar()" alt="" srcset=""/>
        </div>
        <div class="card-details">
            <p class="card-details-name">{{ fullName }}</p>
      <p class="card-details-job">{{ faker.name.jobTitle() }}, {{ faker.name.jobArea() }}</p>
      <p class="card-details-quote">"{{ faker.lorem.paragraph() }}"</p>
        </div>
    </div>
</template>

<style scoped lang="postcss">
.card{
    @apply cursor-pointer overflow-hidden rounded-md bg-slate-100 p-8 
    shadow-md hover:scale-110 
    transition-transform duration-500 hover:shadow-slate-700 
    hover:shadow-2xl;
    &-image{
        img{
             @apply mx-auto rounded-full object-contain
        }
       
    }
    &-details{
        @apply flex flex-col pt-6 text-center;
        &-name{
            @apply text-3xl font-thin tracking-wider text-yellow-800;
        }
        &-job{
            @apply text-xs  text-red-800;
        }
        &-email{
            @apply text-xs text-slate-700 font-bold;
        }
        &-quote{
            @apply text-lg pt-4 italic text-slate-700;
        }
    }
}
</style>