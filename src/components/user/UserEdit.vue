<template>
<div>

    <h3>Edit the User</h3>
    <div>
        <label for="name">Name: </label>
        <input type="text" id="name" placeholder="Enter new name">
    </div>
    <div>
        <label for="password">New password: </label>
        <input type="password" id="password" placeholder="Enter new password">
    </div>
    <div>
        <label for="password2">Repeat new password: </label>
        <input type="password" id="password2" placeholder="Confirm new password">
    </div>
    <button @click="saveChanges">Save</button>
</div>
</template>
<script>
export default {
    data() {
        return {
            savedChanges: false
        }
    },
    methods: {
        saveChanges() {
            this.savedChanges = true; 
            console.log('Changes saved')
        }
    },
    beforeRouteLeave(to, from, next) {
        if (this.savedChanges) {
            next()
        } else {
            if (confirm("Changes are not saved.\nAre you sureyou want to leave?")) {
                next()
            } else {
                next(false)
            }
        }
    }
}
</script>