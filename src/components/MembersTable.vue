<template>
    <v-table
        fixed-header
        justify="center"
        theme="dark"
        class="rounded-lg"
        >
        <thead>
        <tr>
            <th class="text-left">
            Student ID
            </th>
            <th class="text-left">
            Student Name
            </th>
            <th>
            Student Image
            </th>
        </tr>
        </thead>
        <tbody>
        <tr
            v-for="item in members"
            :key="item.studendID"
        >
            <td>{{item.studendID}}</td>
            <td>{{ item.name }}</td>
            <td class="pa-md-6">
                <v-img
                    class="rounded-xl"
                    :width="300"
                    aspect-ratio="16/9"
                    cover
                    :src="item.imageUrl"
                    ></v-img>
            </td>
        </tr>
        </tbody>
    </v-table>
</template>
<script>
export default {
    name: 'MembersTable',
    data(){
        return{
            members:[
                {
                    studendID: 'MCC2021-0382',
                    name: 'Marc Danielle Cabatay',
                    imageUrl:require('@/assets/images/Cabatay.png'),
                },
                {
                    studendID: 'MCC2021-0341',
                    name: 'Ellyssa Golfo',
                    imageUrl:require('@/assets/images/Golfo.jpg'),
                },
                {
                    studendID: 'MCC2021-0379',
                    name: 'Esairah Matira',
                    imageUrl:require('@/assets/images/Matira.jpg'),
                },
            ]
        }
    }
}
</script>
<style>
    
</style>