<template>
  <div>
    <participants-list :list="list"> </participants-list>
    <new-participant-form> @added="addNewParticipant()" </new-participant-form>


</div>
</template>

<script>
  import ParticipantsList from "./ParticipantsList.vue";
  import NewParticipantForm from "./NewParticipantForm.vue";

    export default {
        components: {ParticipantsList, NewParticipantForm},
        data() {
            return { list: [] } ;
        },
        methods: {
            addNewParticipant() {
               // if (!this.Firstname || !this.Lastname) {
                   // return;
                //}

                this.list.push (this.Firstname + ' ' + this.Lastname);
                this.Firstname="";
                this.Lastname="";

            }
        }
    };
</script>