<template>
    <!-- page container -->
    <div class="bg-blue-100 font-body font-thin min-h-screen md:h-screen md:flex flex-col">

        <header class="sticky top-0 md:flex">
            <!-- top bar  -->
            <div class="bg-yellow-500 text-white text-lg flex justify-between py-2 px-4 md:w-56 md:flex-shrink-0">
            <!-- brand -->
            <div class="font-title">HomeDad</div>

            <!-- page title -->
            <div class="md:hidden">Welcome!</div>

            <!-- mobile button -->
            <button
                class="text-xl md:hidden"
                @click="mobileSidebarOpen = !mobileSidebarOpen"
            >
                🍔
            </button>
            </div>

            <!-- mobile sidebar -->
            <aside
                class="bg-yellow-300 w-5/6 fixed inset-y-0 rounded-r-3xl md:hidden transform transition-transform duration-200"
                :class="{'-translate-x-full': !mobileSidebarOpen}"
            >
                <NavMenu />
            </aside>

            <!-- desktop top bar -->
            <div class="hidden bg-yellow-300 text-white py-2 px-4 text-lg md:flex justify-between w-full">
            <div>Welcome!</div>
            <div>username ⚙️</div>
            </div>
        </header>

        <main class="md:flex md:overflow-y-hidden md:flex-grow">
            <!-- desktop sidebar -->
            <aside class="hidden bg-yellow-300 md:block w-56 flex-shrink-0 overflow-y-auto">
                <NavMenu />
            </aside>

            <!-- content container -->
            <div class="p-2 overflow-y-auto">
            <div class="shadow rounded-md bg-white my-2 p-2">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sit, dolor at nesciunt repellat magnam amet ex quam. Dolorem, adipisci. Blanditiis libero animi omnis! Quis debitis quidem earum cupiditate fugiat saepe.</div>
            <div class="shadow rounded-md bg-white my-2 p-2">Quam necessitatibus quae corrupti quas? Cum soluta quia perferendis voluptas, commodi provident fugiat eligendi atque aliquam fuga temporibus optio minus nemo quae quasi corporis itaque rerum. Aspernatur nulla nesciunt quod.</div>
            <div class="shadow rounded-md bg-white my-2 p-2">Voluptates, eligendi. Ipsa nobis quia eos ipsam quibusdam veritatis cumque pariatur quam ab, nesciunt praesentium dolorem vero natus dolor reiciendis minus, corrupti exercitationem doloribus repellendus quidem quis eum distinctio. Pariatur!</div>
            <div class="shadow rounded-md bg-white my-2 p-2">Laborum, perferendis laudantium consectetur culpa quod distinctio cupiditate molestiae earum odio placeat voluptatibus similique voluptatem exercitationem ab eum enim itaque nam optio cum aspernatur officiis sint. Beatae, quisquam. Eaque, sunt!</div>
            <div class="shadow rounded-md bg-white my-2 p-2">Provident assumenda inventore magnam repudiandae! Vero assumenda quidem, modi, dolorum pariatur aliquid qui temporibus ad veritatis provident earum quas perferendis suscipit sit fugit commodi enim dignissimos! Quos nisi rerum natus!</div>
            </div>
        </main>
    </div>
</template>

<script setup>
import { ref } from "@vue/reactivity";
import NavMenu from '@/Components/Layouts/NavMenu';

let mobileSidebarOpen = ref(true);
</script>