<template>
    <li>
        <h2>{{ name }} {{ friendIsFavourite ? '*Favourite' : null }}</h2>
        <button @click="toggleDetails">{{ detailsAreVisible ? 'Hide' : 'Show' }} details</button>
        <button @click="toggleFavourite">Toggle favourite</button>
        <ul v-if="detailsAreVisible">
            <li><strong>Phone:</strong>{{ phoneNumber }}</li>
            <li><strong>Email:</strong>{{ emailAddress }}</li>
        </ul>
    </li>
</template>


<script>
export default {
    props: {
        name: {
            type: String,
            required: true,
        },
        phoneNumber:  {
            type: String,
            required: true
        },
        emailAddress:  {
            type: String,
            required: true
        },
        isFavourite: {
            type: Boolean,
            required: true,
            default: false,
            validator: function(value) {
                return value === '1' || value === '0';
            },
        }
    },
    data() {
        return {
            detailsAreVisible: false,
            friendIsFavourite: this.isFavourite,
        }
    },
    methods: {
        toggleDetails() {
            this.detailsAreVisible = !this.detailsAreVisible;
        },
        toggleFavourite() {
            this.friendIsFavourite = !this.friendIsFavourite;
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