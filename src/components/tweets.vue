<template>
    <div class="tweets-container">
        <h1>TWEETS!</h1>
        <button id="change-view" @click="grid= !grid">Change View</button>
        <div id="grid" :class="{listView: grid}">
            <div id="tweet-area" v-for="tweet in tweets" v-bind:key="tweet"> 
                <h3>{{ tweet.content }}</h3>
                <p>{{ " Posted By: " + tweet.name }}</p>
                <p>{{ " Created On: " + tweet.date }}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "tweets-page",
    data: function(){
        return{
            tweets:[
                {
                    content: "This is my first Tweet!",
                    name: "Rainer",
                    date: "01-18-2020"
                },
                {
                    content: "What's up everyone!",
                    name: "Brandy",
                    date: "04-22-2020"
                },
                {
                    content: "I'm a cat!",
                    name: "Cylus",
                    date: "07-15-2020"
                },
                {
                    content: "Hello Hello! How are you???",
                    name: "Emma",
                    date: "12-05-2019"
                },
                {
                    content: "I'm eating pizza!",
                    name: "Jon",
                    date: "10-27-2019"
                }
            ],
            grid: true,
        }
    },
}
</script>

<style scoped>

    #grid {
        display: grid;
        justify-items: center;
        align-items: center;
        grid-template-rows: repeat(5, 1fr);
        margin: 2vw;
    }
    .listView {
        display: grid;
        justify-items: center;
        align-items: center;
        grid-template-columns: repeat(5, 1fr);
    }

    button {
        font-family: 'Roboto Mono', monospace;
        font-weight: bold; 
        width: 10%;
        background-color: #08a0e9;
        color: #e8f5fd;
        box-shadow: 2px 3px 4px #0084b4 ;
        padding: 10px;
    }

    #tweet-area {
        border: 1px solid black;
        box-shadow: 2px 3px 4px lightslategray;
        padding: 2vw;
        margin: 2vw;
        height: 15vw;
        width: 65%;
    }

</style>