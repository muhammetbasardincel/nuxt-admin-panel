<template>

    <div class="w-screen h-screen bg-slate-800 flex justify-center items-center">

        <div class="w-1/4 py-10 flex justify-center items-center bg-slate-700 flex-col rounded-lg shadow-lg">
            <div class="font-light text-5xl mb-10 text-gray-900">
                Yeni Kayıt
            </div>
            <form @submit.prevent="login" class="space-y-4 font-semibold">
                <div class="w-full space-y-2">
                    <label for="username" class="text-xl">Adınız:</label>
                    <input type="text" id="username" class="w-full py-2 px-4 rounded-lg outline-0 focus:bg-gray-300" v-model="username" autocomplete="off">
                </div>
                <div class="w-full space-y-2">
                    <label for="username" class="text-xl">Soyadınız:</label>
                    <input type="text" id="username" class="w-full py-2 px-4 rounded-lg outline-0 focus:bg-gray-300" v-model="username" autocomplete="off">
                </div>
                <div class="w-full space-y-2">
                    <label for="username" class="text-xl">Email:</label>
                    <input type="text" id="username" class="w-full py-2 px-4 rounded-lg outline-0 focus:bg-gray-300" v-model="username" autocomplete="off">
                </div>
                <div class="w-full space-y-2">
                    <label for="username" class="text-xl">Telefon:</label>
                    <input type="text" id="username" class="w-full py-2 px-4 rounded-lg outline-0 focus:bg-gray-300" v-model="username" autocomplete="off">
                </div>
                <div class="w-full space-y-2">
                    <label for="username" class="text-xl">Şifre:</label>
                    <input type="text" id="username" class="w-full py-2 px-4 rounded-lg outline-0 focus:bg-gray-300" v-model="username" autocomplete="off">
                </div>
                <div class="w-full space-y-2">
                    <label for="password" class="text-xl">Şifre Tekrar:</label>
                    <input type="password" id="password" class="w-full py-2 px-4 rounded-lg outline-0 focus:bg-gray-300" v-model="password" autocomplete="off">
                </div>
                <div>
                    <button type="submit" class="bg-slate-800 text-slate-200 border-black border-2 p-2 rounded-xl hover:bg-slate-200 hover:text-slate-900 transition ease-in-out ">Hesap Aç</button>
                </div>
                <div v-if="error">{{ error }}</div>
            </form>

        </div>



    </div>


</template>

<script>
export default {
    name: "register"
}
</script>

<style scoped>

</style>