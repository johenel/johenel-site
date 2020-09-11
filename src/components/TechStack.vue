<template>
    <div id="skills" class="tw-w-full">
        <div class="tw-flex tw-flex-row tw-flex-wrap tw-grid tw-grid-cols-3 " >
            <div v-for="(v, i) in techs" :key="i" class="tw-p-2 tw-py-4 tw-pt-6 tw-mx-auto" style="width: 90%;position:relative">
                <label :class="v.label_class">{{v.label}}</label>
                <div class="stack tw-flex tw-flex-row tw-flex-wrap tw-justify-center tw-mb-12">
                    <div v-for="(value, index) in v.stack" :key="index" class="tw-px-3 tw-py-1">
                        <v-chip class="ma-1" label>{{value}}</v-chip>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'TechStack',
    data() {
        return {
            techs: [
                {
                    label: 'Back End',
                    label_class: 'tw-bg-blue-700 ',
                    stack: [
                        'PHP', 'Laravel', 'Restful API', 'composer'
                    ]
                },
                {
                    label: 'Front End',
                    label_class: 'tw-bg-green-700 tw-px-4',
                    stack: [
                        'VueJS', 'Tailwind CSS', 'NPM', 'NodeJS', 'javascript', 'jQuery', 'CSS', 'LESS', 'HTML'
                    ]
                },
                {
                    label: 'Database',
                    label_class: 'tw-bg-purple-700 tw-px-4',
                    stack: [
                        'MySQL'
                    ]
                },
                {
                    label: 'Servers',
                    label_class: 'tw-bg-orange-700 tw-px-4',
                    stack: [
                        'Linux/CentOS'
                    ]
                },
                {
                    label: 'Versioning Tool',
                    label_class: 'tw-bg-gray-700 tw-px-4',
                    stack: [
                        '.git'
                    ]
                }
            ]
        }
    }
}
</script>

<style scoped>
    label {
        @apply tw-px-4 tw-py-2 rounded;
        position: absolute;
        top: -2rem;
        left: 0px;
        right: 0px;
        margin: auto;
        width: fit-content;
        color:white;
    }
</style>