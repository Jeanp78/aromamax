<template>
    <div class="py-4 px-32 border border-black">
        <Divider></Divider>
        <Carousel class="w-full " :opts="{
            align: 'center',
        }">
            <CarouselContent class="-ml-1">
                <CarouselItem v-for="product in newProducts" :key="product.id" class=" md:basis-1/2 lg:basis-1/5">
                    <Product :name="product.name" :description="product.description"></Product>
                </CarouselItem>
            </CarouselContent>
            <CarouselPrevious />
            <CarouselNext />
        </Carousel>
    </div>
</template>

<script setup lang="ts">
import { Carousel, CarouselContent, CarouselItem, CarouselNext, CarouselPrevious } from '@/components/ui/carousel'
import Divider from '@/components/Divider.vue'
import Product from '@/components/Product.vue'
import newProducts from '@/mocks/newProducts.json'
</script>