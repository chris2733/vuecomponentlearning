<template>
    <section>
        <h2>MY mates</h2>
        <h4>a few</h4>
        <ul>
            <friend-contact></friend-contact>
            <friend-contact></friend-contact>
        </ul>
    </section>
</template>

<script>
export default {
    data() {
        return {
            friends: [
                {
                    id: 'manuel',
                    name: 'Manuel Iglesias',
                    phone: '1235345 23432',
                    email: 'manuel@iglesias.esp'
                },
            ]
        }
    }
}
</script>