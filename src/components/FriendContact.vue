<template>
    <li>
        <h2>{{ name }}</h2>
        <button @click="toggleDetails">{{ this.detailsAreVisible ? 'Hide' : 'Show' }} details</button>
        <ul v-if="detailsAreVisible">
            <li><strong>Phone:</strong>{{ phoneNumber }}</li>
            <li><strong>Email:</strong>{{ emailAddress }}</li>
        </ul>
    </li>
</template>


<script>
export default {
    props: [
        'name',
        'phoneNumber',
        'emailAddress'
    ],
    data() {
        return {
            detailsAreVisible: false,
        }
    },
    methods: {
        toggleDetails() {
            this.detailsAreVisible = !this.detailsAreVisible;
        }
    }
};
</script>


<style lang="scss">
button {
    background: green;
    &::before {
        content: '';
        width: 5px;
        height: 15px;
        background: blue;
    }
}
</style>