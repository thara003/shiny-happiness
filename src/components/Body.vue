<template>
    <div class="px-4">
        <div v-for="message in messages" v-bind:key="message.id">
            <Message :strong1="message.strong1" :text="message.text" :strong2="message.strong2"
                :timeago="message.timeago" :listitem="message.listitem" />
            <hr class="my-3" />
        </div>
    </div>
</template>
<script>
import Message from './Message.vue';
export default {
    components: {
        Message,
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
                },
                {
                    id: 2,
                    strong1: 'Jason Raddon ',
                    text: 'mention you in 😍 ',
                    strong2: 'Tennis List',
                    timeago: '4h ago ',
                    listitem: 'Hobby List',
                },
                {
                    id: 3,
                    strong1: 'Sandra Marx ',
                    text: 'is requesting to upgrade plane',
                    strong2: '',
                    timeago: '12h ago ',
                    listitem: 'Hobby List',
                },
                {
                    id: 4,
                    strong1: 'Adam Smith ',
                    text: 'upload a file',
                    strong2: '',
                    timeago: '1d ago ',
                },
                {
                    id: 5,
                    strong1: 'Ralpg Turner ',
                    text: 'edited 🥂 ',
                    strong2: 'Celebrate info',
                    timeago: '4h ago ',
                    listitem: 'Hobby List',
                },
                {
                    id: 6,
                    strong1: 'Dan Merix ',
                    text: 'is requesting to upgrade plane',
                    strong2: '',
                    timeago: '12h ago ',
                    listitem: 'Hobby List',
                },
                {
                    id: 7,
                    strong1: 'Anna Srzand ',
                    text: 'joined to 🔥 ',
                    strong2: 'Final Presentation',
                    timeago: '2h ago ',
                    listitem: 'Social Media Plan',
                },
                {
                    id: 8,
                    strong1: 'Jason Raddon ',
                    text: 'mention you in 😍 ',
                    strong2: 'Tennis List',
                    timeago: '4h ago ',
                    listitem: 'Hobby List',
                },
                {
                    id: 9,
                    strong1: 'Sandra Marx ',
                    text: 'is requesting to upgrade plane',
                    strong2: '',
                    timeago: '12h ago ',
                    listitem: 'Hobby List',
                },
                {
                    id: 10,
                    strong1: 'Adam Smith ',
                    text: 'upload a file',
                    strong2: '',
                    timeago: '1d ago ',
                },
                
            ],
        }
    }


};
</script>