<template>
    <div class="bg-white py-24 sm:py-32">
        <div class="mx-auto grid max-w-7xl gap-x-8 gap-y-20 px-6 lg:px-8 xl:grid-cols-3">
            <div class="max-w-2xl">
                <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Meet our Group</h2>
                <p class="mt-6 text-lg leading-8 text-gray-600">We hope you'll have a great time during your visit. Each of us brings unique 
                    abilities, and effective communication is key to harnessing our 
                    distinct features for the success of our upcoming projects.</p>
            </div>
            <ul role="list" class="grid gap-x-8 gap-y-12 sm:grid-cols-2 sm:gap-y-16 xl:col-span-2">
                <li v-for="person in people" :key="person.name">
                    <div class="flex items-center gap-x-6">
                    <img class="h-20 w-20 rounded-full" :src="person.imageUrl" alt="" />
                    <div>
                        <h3 class="text-base font-semibold leading-7 tracking-tight text-gray-900">{{ person.name }}</h3>
                        <p class="text-sm font-semibold leading-6 text-indigo-600">{{ person.role }}</p>
                    </div>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default{
    name: 'TeamSection',
    data(){
        return{
            people : [
                    {
                        name: 'Marc Danielle Cabatay',
                        role: 'Programmer',
                        imageUrl:
                            require('@/assets/images/Cabatay.png'),
                        },
                    {
                        name: 'Ellyssa Golfo',
                        role: 'Programmer',
                        imageUrl:
                            require('@/assets/images/Golfo.jpg'),
                    },
                    {
                        name: 'Esairah Matira',
                        role: 'Programmer',
                        imageUrl:
                            require('@/assets/images/Matira.jpg'),
                    },
                    // More people...
                ]
        }
    }
}  
</script>