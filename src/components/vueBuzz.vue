<template>
    <div>
        <h1>VueBuzz Game</h1>
        <div v-for="number in numbers" :key="number">
            <p>{{ getResult(number) }}</p>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            //Create an array from 0 to 100
            numbers: Array.from({ length: 100 }, (_, index) => index + 1)
        };
    },
    methods: {
        getResult(number) {
            let result = '';
            if (number % 3 === 0) {
                result += 'Vue';
            }
            if (number % 5 === 0) {
                result += 'Buzz';
            }
            return result || number;
            
        }
    }
};
</script>