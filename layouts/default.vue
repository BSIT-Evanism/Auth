<template>

    <div class="bg-#e9e6e4 box-content font-mono m-0">
        <div class="h-5 w-5 rounded-xl absolute top-4 right-4 bg-black lg:hidden md:hidden" @click="toggle"></div>
        <div class="flex bg-#e9e6e4">

            <aside v-if="val" class="flex b-t-1 h-70vh relative group h-50% b-0  border-solid bg-#e9e6e4 w-44 flex-col hover:p-8 hover:animate-pulse animation-all duration-300ms">
                <NuxtLink class="p4 static text-xl h-2 w-20 m-5 font-bold no-underline text-slate-400 group-hover:text-slate-700 hover:translate-x-2 hover:before:content-['=>'] hover:duration-300ms animate-all duration-700ms" to="/">Home</NuxtLink>
                <NuxtLink class="p4 static text-xl h-2 w-20 m-5 font-bold no-underline text-slate-400 group-hover:text-slate-700 hover:translate-x-2 hover:before:content-['=>'] hover:duration-300ms animate-all duration-700ms" to="/about">About</NuxtLink>
                <NuxtLink class="p4 static text-xl h-2 w-20 m-5 font-bold no-underline text-slate-400 group-hover:text-slate-700 hover:translate-x-2 hover:before:content-['=>'] hover:duration-300ms animate-all duration-700ms" to="/articles">Articles</NuxtLink>
                <NuxtLink class="p4 static text-xl h-2 w-20 m-5 font-bold no-underline text-slate-400 group-hover:text-slate-700 hover:translate-x-2 hover:before:content-['=>'] hover:duration-300ms animate-all duration-700ms" to="/people">People</NuxtLink>
                <carousel class="relative" />
            </aside>
            <div v-else>test</div>
        
                <slot />
        
        </div>

        <div class="group">
            
            
            <div class="fixed w-100% flex justify-center flex-col bottom-4">
                <div class="absolute justify-center bottom-0 z-1 w-screen border-t-1 border-b-1 border-l-0 border-r-0 border-solid group-hover:translate-y--37 animate-all duration-500ms bg-slate-200 ">
                    <marquee behavior="alternate" scrollamount="1" scrolldelay="30" direction="left">
                        <span>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nesciunt, dolorem a ad soluta nam debitis iure quos nisi inventore expedita?</span>
                        <span>Testn 2 </span>
                        <span>Test 3 </span>
                    </marquee>
                </div>
                <footers class="" />
            </div>
        </div>
    </div>
</template>

<script setup>

const val = ref(true)

function toggle() {
    val.value = !val.value
    console.log(val.value)
}

</script>

<style scoped>


</style>
