<template>
    <active-user :userName="user" :age="userAge"></active-user>
    <user-data @update-userage="updateAge" @update-username="updateUser"></user-data>
</template>


<script>
export default {
    data() {
        
    return {user: "Bilal", userAge: "28"};
    },
    methods: {
        updateUser(name){
            this.user = name;
        },
        updateAge(age){
            this.userAge = age;

        }
    }
    

}
</script>