<template>
    <Carousel :opts="carouselOptions" class="relative w-full ">
        <CarouselContent>
            <CarouselItem v-for="(_, index) in 5" :key="index">
                <img class="w-full"
                    src="https://media.maxaroma.com/9cd29e92-4b8f-436f-ad1f-8e368b30dc1d/https://www.maxaroma.com/images/homeimg/banner_72024-05-13-17-05-06.jpg?ver=1715619966"
                    alt="">
            </CarouselItem>
        </CarouselContent>
    </Carousel>
</template>

<script setup lang="ts">
import { Carousel, CarouselContent, CarouselItem } from '@/components/ui/carousel'

const carouselOptions = {
    // align: 'start',
    loop: true,
}
</script>
