<script setup>
const url = 'http://127.0.0.1:3000/api/users'

const users = useFetch(url, { pick: ["name", "email", "password"] })

console.log(users)
</script>