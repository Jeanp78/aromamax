<template>
    <header class=" flex flex-col border-b border-gray-300 ">
        <div class="flex justify-center gap-2  bg-black px-10">
            <Button class="text-white" variant="link"> Est minim laboris eu culpa commodo.
            </Button>
            <Button class="text-white" variant="link">Aute esse mollit non do ut.</Button>
            <Button class="text-white" variant="link">lorem ipsum</Button>
        </div>
        <div class="py-2 flex  gap-4 justify-center w-3/4 m-auto">
            <img src="https://placehold.co/200x70" width="200" height="100">
            <div class=" w-full">
                <div class="  flex gap-2 justify-end items-center">
                    <div class="relative w-410 items-center">
                        <Input id="search" type="text" placeholder="Buscar un producto" class="pl-10" />
                        <span class="absolute start-0 inset-y-0 flex items-center justify-center px-2">
                            <MagnifyingGlassIcon class="size-6 text-muted-foreground" />
                        </span>
                    </div>
                    <Select>
                        <SelectTrigger class="w-[100px]">
                            <SelectValue :placeholder="currencies[0]" />
                        </SelectTrigger>
                        <SelectContent>
                            <SelectGroup>
                                <SelectLabel>Moneda</SelectLabel>
                                <SelectItem v-for="currency in currencies" value="USD">
                                    {{ currency }}
                                </SelectItem>
                            </SelectGroup>
                        </SelectContent>
                    </Select>
                </div>
                <div class=" flex justify-between items-center  h-1/2">
                    <Button v-for="menu in menus" size="sm" class="uppercase font-bold" variant="link">{{ menu
                        }}</Button>
                    <div class="flex items-center gap-1">
                        <AvatarIcon class="size-6"></AvatarIcon>
                        <ArchiveIcon class="size-6"></ArchiveIcon>
                    </div>
                </div>
            </div>
        </div>
    </header>

</template>

<script setup>
import { AvatarIcon } from '@radix-icons/vue';
import { MagnifyingGlassIcon, ArchiveIcon } from '@radix-icons/vue'
import { Input } from '@/components/ui/input'
import { Button } from '@/components/ui/button'
import {
    Select,
    SelectContent,
    SelectGroup,
    SelectItem,
    SelectLabel,
    SelectTrigger,
    SelectValue,

} from '@/components/ui/select'
import { ref } from 'vue';

const menus = [
    'Culpa incididunt adipisicing',
    'Non nisi ea',
    'Aliquip cupidatat.',
    'Sunt deserunt',
    'Consequat commodo',
    'Elit nulla'
]

const currencies = ['COP', 'USD']
const showSubcategories = ref(false);


</script>