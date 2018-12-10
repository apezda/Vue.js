<template>
  <div>
    <div>
      <h1 v-if="list.length > 0" > Participants list </h1>
      <ol>
        <li v-for="person in list"> {{person}}</li>
      </ol>
    </div>

    <h3>New participant</h3>
    <form @submit.prevent="addNewParticipant()">
      <label>Firstname</label>
      <input type="text" v-model="Firstname">
      <label>Lastname</label>
      <input type="text" v-model="Lastname">
      <button> Add new participant</button>
    </form>
  </div>
</template>

<script>
    export default {
        data() {
            return { list: [] } ;
        },
        methods: {
            addNewParticipant() {
                if (!this.Firstname || !this.Lastname) {
                    return;
                }

                this.list.push (this.Firstname + ' ' + this.Lastname);
                this.Firstname="";
                this.Lastname="";

            }
        }
    };
</script>