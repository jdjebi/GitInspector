<template>
    <div class="fw-bold text-success small">TOP par qualité de profil</div>
    <div class="table-responsive">
        <table class="table table-lg">
            <thead>
                <tr>
                    <th>#Rang</th>
                    <th>Candidat</th>
                    <th>Score</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(candidat, index) in candidats" v-bind:key="candidat">
                    <td>{{ index + 1 }}</td>
                    <td>
                        <img v-bind:src="candidat.avatar_url" alt="" width="25" height="25" class="border rounded-circle">
                        &nbsp; {{ candidat.login }}
                    </td>
                    <td>{{ candidat.score }}</td>
                </tr>
            </tbody>        
        </table>
    </div>
</template>

<script>

export default {

    name:"TableFollowing",

    props: ["candidats"],
}
</script>

<style scoped>

</style>