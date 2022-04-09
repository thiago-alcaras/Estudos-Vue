<template>
    <div class="">
        <input type="text" v-model="text"/>
        <span>Text: {{text}}</span>
        <span>Api: {{apiResponse}}</span>
    </div>
</template>

<script>
export default {
    name: 'ApiResponse',
    data() {
        return {
            apiResponse:"Start",
            text: ''
        }
    },
    methods: {
        simulateApi(response) {
            return new Promise(() => {
                setTimeout(() => {
                    this.apiResponse = response;
                }, 1000);
            });
        },

        async fetchApi(value){
            await this.simulateApi(value);
        },

        callApi(newValue, oldValue){
            if(newValue.length > 3 && newValue != oldValue) {
                this.fetchApi(newValue);
            }
        }
    },
    watch: {
        text: [
            'callApi',
            function handler2(val){
                this.fetchApi(val);
            }
        ]
    }
}
</script>

<style>

</style>