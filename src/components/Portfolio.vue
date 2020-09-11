<template>
    <div class="tw-flex tw-flex-col " style="max-width:600px">
        <v-card v-for="(value, index) in projects" :key="index" class="tw-mb-10 ">
            <v-card-title>{{value.name}}</v-card-title>
            <v-card-subtitle><a :href="value.link" target="_blank">{{value.link}}</a></v-card-subtitle>
            <v-card-subtitle class="tw-pt-0 tw-text-black">{{value.duration}}</v-card-subtitle>
            <v-card-text>{{value.description}}</v-card-text>
            <v-carousel
                height="400"
                show-arrows-on-hover
            >
                <v-carousel-item
                v-for="(v,i) in value.images"
                :key="i"
                :src="v"
                reverse-transition="fade-transition"
                transition="fade-transition"
                ></v-carousel-item>

            </v-carousel>
        </v-card>
    </div>
</template>
<script>
export default {
    name: 'Portfolio',
    data() {
        return {
            projects: [
                {
                    name: 'Percdc Learn Hub',
                    link: 'https://percdclearnhub.org',
                    description: 'A web app that is designed for online learning. Teachers can create exams, upload learning materials such as videos, pdf, documents, etc; and create classes. While studens can join classes, access learning materials such as watching videos and downloading documents.',
                    duration: 'June - August, 2020',
                    features: [
                        'Blogs/Posts',
                        'Exam creator',
                        'Class organizer',
                        'Learning materials organizer'
                    ],
                    images: [
                        '/images/portfolio/percdclearnhub/1.png',
                        '/images/portfolio/percdclearnhub/2.png',
                        '/images/portfolio/percdclearnhub/3.png',
                        '/images/portfolio/percdclearnhub/4.png',
                        '/images/portfolio/percdclearnhub/5.png',
                    ]
                },
                {
                    name: 'Trihomebased',
                    link: '(dead)',
                    duration: '2019',
                    description: 'A web app that let the user earn by just entering captchas',
                    features: [
                        'captcha'
                    ],
                    images: [
                        '/images/portfolio/trihomebased/1.png',
                        '/images/portfolio/trihomebased/2.png',
                        '/images/portfolio/trihomebased/3.png',
                        '/images/portfolio/trihomebased/4.png',
                    ]
                },
                {
                    name: 'Runkitek',
                    link: '(dead)',
                    duration: '2019',
                    description: 'An advertisement page of a marathon event (Runkitek).',
                    features: [],
                    images: [
                        '/images/portfolio/runkitek/1.png',
                        '/images/portfolio/runkitek/2.png',
                        '/images/portfolio/runkitek/3.png',
                        '/images/portfolio/runkitek/4.png',
                        '/images/portfolio/runkitek/5.png',
                        '/images/portfolio/runkitek/6.png',
                        '/images/portfolio/runkitek/7.png',
                    ]
                }
            ]
        }
    }
}
</script>