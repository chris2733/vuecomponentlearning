<template>
    <li>
        <h2>{{ friend.name }}</h2>
        <button @click="toggleDetails">{{ this.detailsAreVisible ? 'Hide' : 'Show' }} details</button>
        <ul v-if="detailsAreVisible">
            <li><strong>Phone:</strong>{{ friend.phone }}</li>
            <li><strong>Email:</strong>{{ friend.email }}</li>
        </ul>
    </li>
</template>


<script>
export default {
    data() {
        return {
            detailsAreVisible: false,
            friend: {
                id: 'manuel',
                name: 'Manuel Iglesias',
                phone: '1235345 23432',
                email: 'manuel@iglesias.esp'
            },
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