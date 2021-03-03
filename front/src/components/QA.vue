<template>
    <div>
        <h2 class="eng">{{ question }}</h2>
        <hr>
        <h3 class="ee">Sinu Vastus</h3>
        <textarea name="ans" id="ans" cols="15" rows="5" class="ee" @keyup.enter="onSubmit"></textarea>
    </div>
</template>

<script>
export default {
    name: "QA",
    props: {
        question: String
    },
    methods: {
        onSubmit(event) {
            const user_ans = event.target.value.toLowerCase();
            console.log(user_ans);
        }
    }
}
</script>

<style scoped>
    @font-face {
        font-family: "AinoR";
        src: url("../assets/Aino-Regular.woff");
    }
    @font-face {
        font-family: "AinoH";
        src: url("../assets/Aino-Headline.woff");
    }
    h2, h3 {
        margin: auto;
        text-align: center;
    }
    h3 {
        margin-bottom: 10px;
    }
    textarea {
        display: block;
        margin: 0 auto;
        text-align: center;
        font-size: 20px;
        border-radius: 5px;
    }
    .eng {
        font-family: "AinoR";
        font-weight: lighter;
    }
    .ee {
        font-family: "AinoH";
    }
</style>