<script setup>
import MainSearch from '@/components/MainSearch.vue'
import mainCards from '@/components/mainCards.vue'
import mainPagination from '@/components/mainPagination.vue'
</script>

<template>
    <div class="wrapper">
        <MainSearch />
        <mainCards />
        <mainPagination />
    </div>
</template>

<style scoped lang="postcss">
.wrapper{
    @apply container mx-auto flex flex-col py-4 gap-4;
}
</style>