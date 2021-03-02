<template>
    <div>
        <h1>ini adalah form pendaftaran</h1>
        <form @submit="postData" method="post">
            <input
                type="text"
                name="username"
                placeholder="masukkan username"
                v-model="datas.username"
            />
            <br /><br />
            <input
                type="text"
                name="email"
                placeholder="masukkan email"
                v-model="datas.email"
            />
            <br /><br />
            <input
                type="text"
                name="password"
                placeholder="masukkan password"
                v-model="datas.password"
            />
            <br /><br />
            <button type="submit">Submit</button>
        </form>
    </div>
</template>

<script>
export default {
    name: "FormPendaftaran",
    data() {
        return {
            datas: {
                username: null,
                email: null,
                password: null,
            },
        }
    },
    methods: {
        postData(e) {
            console.log(this.datas)
            e.preventDefault()
        },
    },
}
</script>
