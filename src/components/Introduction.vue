<template>
    <div class="tw-flex tw-flex-row tw-grid lg:tw-grid-cols-2 sm:tw-grid-cols-1">
        <div class="tw-flex profile-picture content-center justify-center">
            <v-avatar size="300">
                <img
                    height="100%"
                    src="../../public/images/jojie.jpg"
                    alt="Johenel Labayan"
                >
            </v-avatar>
        </div>
        <div class="tw-flex information tw-flex tw-flex-col sm:tw-text-center lg:tw-lext-left">
            <h2 class="name">Johenel P. Labayan</h2>
            <p class="title">Web Developer (Laravel/PHP)</p>
            <p class="pitch" style="width:95%">
                Good day! I am a Laravel developer with 4 years experience. I started web development as a backend developer, used in developing projects with MVC structure.
                I have also experience in developing Restful API projects. The frontend framework I am proficient the most is VueJS (CLI). I have deployed and maintained
                projects using Linux server (Digital Ocean & Godaddy). The database I used on the projects I have worked with is MySQL.         
            </p>
        </div>
    </div>
</template>

<style scoped>
    .v-avatar {
    }
    @media(max-width: 1023px) {
        .v-avatar {
            height: 250px !important;
            min-width: 250px !important;
            width: 250px !important;
        }

        h2.name {
            font-size: 2rem;
        }
    }
</style>