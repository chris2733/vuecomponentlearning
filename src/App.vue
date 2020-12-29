<template>
  <section>
    <h2>MY mates</h2>
    <h4>a few</h4>
    <ul>
	<friend-contact
		v-for="friend in friends"
		:key="friend.id"
		:name="friend.name"
		:phone-number="friend.phoneNumber"
		:email-address="friend.emailAddress"
		:is-favourite="friend.isFavourite"
	>
	</friend-contact>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      friends: [
        {
			id: "manuel",
			name: "Manuel Iglesias",
			phoneNumber: "1235345 23432",
			emailAddress: "manuel@iglesias.esp",
			isFavourite: true,
        },
        {
			id: "janey",
			name: "JLO Iglesias",
			phoneNumber: "77745 23444",
			emailAddress: "jlo@iglesias.esp",
        },
      ],
    };
  },
};
</script>
