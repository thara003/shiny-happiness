<template>
    <div class="mb-8">
        <div v-for="message in messages" v-bind:key="message.id" :class="[message.id === 1 || message.id === 2 ? 'bg-color' : '']">
            <Message :strong1="message.strong1" :text="message.text" :strong2="message.strong2"
                :timeago="message.timeago" :listitem="message.listitem" :button="message.button"
                :upload="message.upload" :strike="message.strike" :src="message.src" :status = "message.status" :display="message.display"/>
            <hr class ="mx-6 color"/>
        </div>
        <Skeleton class="my-4 px-6"/>
        <hr class="mx-6 color" />
        <Skeleton class="mt-4 px-6"/>
    </div>
</template>
<style>
.bg-color {
    background-color: #fdf7f2;
}
.color {
    border-color: #efeeee;
}
</style>
<script>
import { defineComponent } from 'vue';
import Message from './Message.vue';
import Skeleton from './Skeleton.vue';
export default defineComponent ({
    components: {
    Message,
    Skeleton
},
    data() {
        return {
            messages: [
                {
                    id: 1,
                    strong1: 'Anna Srzand ',
                    text: 'joined to 🔥 ',
                    strong2: 'Final Presentation',
                    timeago: '2h ago ',
                    listitem: 'Social Media Plan',
                    status : 'active',
                    src:'https://images.unsplash.com/photo-1477118476589-bff2c5c4cfbb?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=200&q=200',
                },
                {
                    id: 2,
                    strong1: 'Jason Raddon ',
                    text: 'mention you in 😍 ',
                    strong2: 'Tennis List',
                    timeago: '4h ago ',
                    listitem: 'Hobby List',
                    display: "2",
                },
                {
                    id: 3,
                    strong1: 'Sandra Marx ',
                    text: 'is requesting to upgrade plane',
                    strong2: '',
                    timeago: '12h ago ',
                    listitem: 'Hobby List',
                    button: true,
                    status : 'offline',
                    src: 'https://images.unsplash.com/photo-1529626455594-4ff0802cfb7e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MjZ8fHBlb3BsZXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=800&q=60',
                },
                {
                    id: 4,
                    strong1: 'Adam Smith ',
                    text: 'upload a file',
                    strong2: '',
                    timeago: '1d ago ',
                    upload: true,
                    src: 'https://images.unsplash.com/photo-1539571696357-5a69c17a67c6?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80',
                },
                {
                    id: 5,
                    strong1: 'Ralpg Turner ',
                    text: 'edited 🥂 ',
                    strong2: 'Celebrate info',
                    timeago: '4h ago ',
                    listitem: 'Hobby List',
                    strike: true,
                    display: "5",
                },
                {
                    id: 6,
                    strong1: 'Dan Merix ',
                    text: 'is requesting to upgrade plane',
                    strong2: '',
                    timeago: '12h ago ',
                    listitem: 'Hobby List',
                    button: true,
                    status : 'offline',
                    src: 'https://images.unsplash.com/photo-1501196354995-cbb51c65aaea?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MjN8fHBlb3BsZXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=800&q=60',
                },

            ],
        }
    }


});
</script>