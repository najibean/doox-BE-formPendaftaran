<template>
    <div>
        <h1>Form Pendaftaran</h1>
        <br />
        <br />
        <b-form
            @submit="onSubmit"
            v-if="show"
            method="post"
            style="width: 600px"
            class="mx-auto"
        >
            <b-form-group
                id="input-group-1"
                label="Email address:"
                label-for="input-1"
                style="text-align: left; font-weight: bold"
            >
                <b-form-input
                    id="input-1"
                    v-model="form.email"
                    type="email"
                    placeholder="name@example.com"
                    required
                ></b-form-input>
            </b-form-group>

            <b-form-group
                id="input-group-2"
                label="Your username:"
                label-for="input-2"
                style="text-align: left; font-weight: bold"
            >
                <b-form-input
                    id="input-2"
                    v-model="form.username"
                    placeholder="contoh: doox"
                    required
                ></b-form-input>
            </b-form-group>

            <b-form-group
                id="input-group-3"
                label="Your Password:"
                label-for="input-3"
                style="text-align: left; font-weight: bold"
            >
                <b-form-input
                    id="input-3"
                    v-model="form.password"
                    placeholder="contoh: katakunci"
                    required
                ></b-form-input>
            </b-form-group>

            <b-button type="submit" variant="primary">Daftar</b-button>
        </b-form>
    </div>
</template>

<script>
import Vue from "vue"
import axios from "axios"
import VueAxios from "vue-axios"

Vue.use(VueAxios, axios)

export default {
    name: "Daftar",
    data() {
        return {
            form: {
                email: "",
                username: "",
                password: "",
            },
            show: true,
        }
    },
    methods: {
        onSubmit(event) {
            console.log(this.form)
            this.axios
                .post("http://localhost:3000/api/v1/user/daftar", this.form)
                .then((res) => console.log(res.data))
            alert("Selamat! anda sudah terdaftar.")
            event.preventDefault()

            this.form.email = ""
            this.form.username = ""
            this.form.password = ""
        },
    },
}
</script>
