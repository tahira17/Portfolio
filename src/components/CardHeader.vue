<template>
    <div class="">
        <ul class="flex justify-center">
            <li>
                <RouterLink to="/"
                    class="m-1 px-4 py-2 border-2 border-purple-600 rounded-full hover:bg-purple-600 hover:text-white hover:transition-all hover:duration-300 dark:text-white ">
                    Home</RouterLink>
                <RouterLink to="/about"
                    class="m-1 px-4 py-2 border-2 border-purple-600 rounded-full hover:bg-purple-600 hover:text-white hover:transition-all hover:duration-300 dark:text-white">
                    About</RouterLink>
                <RouterLink to="/gitproject"
                    class="m-1 px-4 py-2 border-2 border-purple-600 rounded-full hover:bg-purple-600 hover:text-white hover:transition-all hover:duration-300 dark:text-white">
                    Git Projects</RouterLink>
                    <RouterLink to="/liveproject"
                    class="m-1 px-4 py-2 border-2 border-purple-600 rounded-full hover:bg-purple-600 hover:text-white hover:transition-all hover:duration-300 dark:text-white">
                    Live Projects</RouterLink>
            </li>
        </ul>


        <div>
            <hr class="border-1 my-8 border-gray-400 sm:w-4/12 mx-auto">
        </div>
    </div>
</template>
<script setup>
import router from '../router';

const route = router.currentRoute.value.path;
</script>