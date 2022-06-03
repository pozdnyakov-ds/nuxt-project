<template>
    <div>
        <h1>Users</h1>
        <ul>
            <li for="user of 5" :key="user">
                <a href="#" click.prevent="userClick(user)">User {{user}}</a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    methods: {
        userClick() {
            
        }
    }
} 
</script>