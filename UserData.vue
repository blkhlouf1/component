<template>
    <div>
        <label for="username">Username</label>
        <input type="text" name="username" v-model="userName" @input="updateUserName">
    </div>
    <div>
        <label for="age">Age</label>
        <input type="text" name="age" v-model="userAge" @input="$emit('update-userage',this.userAge)">
    </div>
 
</template>


<script>
export default {
    emits: ['update-userage', 'update-username'],
    data() {
        return {userName: '', userAge: ''};
    
    },
    methods:{
        updateUserAge(){
            this.$emit('update-userage',this.userAge);
        },
        updateUserName(){
            this.$emit('update-username',this.userName)
        }
    }   
}
</script>