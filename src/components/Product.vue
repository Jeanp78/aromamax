<template>
    <Card class="w-[250px] rounded-none border-none shadow-none hover:shadow-xl">
        <CardHeader class="p-3">
            <img class="max-w-full"
                src="https://media.maxaroma.com/9cd29e92-4b8f-436f-ad1f-8e368b30dc1d/https://www.maxaroma.com/productimages/large/TBDADayattheBarbers.jpg?ver=1713821771"
                alt="">
        </CardHeader>
        <CardContent>
            <div class="flex justify-center">hola</div>
            <h1 class="text-sm font-medium text-center">{{ props.name }}</h1>
            <p class="text-gray-600 leading-4 text-xs text-center">{{ props.description }}</p>
            <p class="text-md font-medium text-center mt-2">$250</p>
        </CardContent>
    </Card>
</template>

<script setup lang='ts'>
import {
    Card,
    CardContent,
    CardHeader,
} from '@/components/ui/card'

const props = defineProps({ name: String, description: String })


</script>