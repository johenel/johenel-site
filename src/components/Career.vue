<template>
    <div class="tw-flex tw-content-center tw-justify-center" style="width:100%">
        <v-timeline
            dense
        >
            <v-timeline-item
                v-for="(value, index) in works"
                :key="index"
                small
                color="pink"
            >
                <h3>{{value.company}}</h3>
                <h4 class="tw-text-blue-600">{{value.position}}</h4>
                <br>
                <p class="tw-text-green-700" style="font-weight:bold">{{value.tenure.from}} - {{value.tenure.to}}</p>
                <p class="tw-text-gray-700">{{value.description}}</p>
                <div class="tw-p-3">
                    <b>Responsibilities:</b>
                    <ul class="tw-mt-2" style="max-width:500px">
                        <li v-for="(v,i) in value.responsibilities" :key="i" class="tw-p-1">
                            {{v}}
                        </li>
                    </ul>
                </div>

            </v-timeline-item>
        </v-timeline>
    </div>
</template>
<script>
export default {
    name: 'Career',
    data() {
        return {
            works: [
                {
                    company: 'Aloware (https://aloware.com)',
                    position: 'Soft Engineer (Fullstack Web)',
                    description: 'Contact Center Software (USA)',
                    tenure: {
                        from: 'Sep. 2020',
                        to: 'Current'
                    },
                    responsibilities: [
                        'Planning and designing features',
                        'Maintain and Develop new features',
                        'Worked with features integrated with third party APIs such as Hubspot, Zapier and Pipedrive',
                    ]
                },
                {
                    company: 'EMAPTA',
                    position: 'Back-End Developer (PHP/Laravel)',
                    description: 'An Off-shoring company. (Australia)',
                    tenure: {
                        from: 'Sep. 2019',
                        to: 'Jun. 2020'
                    },
                    responsibilities: [
                        'Develop a Restful API system based on the company owned mortgage/lending system',
                        'Maintain and fix bugs of existing projects',
                        'Develop new features for the existing projects'
                    ]
                },
                {
                    company: 'Ziosoft',
                    position: 'Web Developer (PHP/Laravel)',
                    description: 'A software as a service based company. (Korea)',
                    tenure: {
                        from: 'Mar. 2019',
                        to: 'Sep. 2019'
                    },
                    responsibilities: [
                        'To maintain and fix bugs of the existing in-house CRM system that caters korean customer service center',
                        'To be able to develop new pages and features for the in-house CRM system'
                    ]
                },
                {
                    company: 'Primzen (contractual)',
                    position: 'Web Developer (PHP/Laravel)',
                    descriotion: 'A product based company. (USA)',
                    tenure: {
                        from: 'Mar. 2018',
                        to: 'Mar. 2019'
                    },
                    responsibilities: [
                        'To be able to develop a Restful API system that will serve a mobile application that focus on providing cancer patients diet routine; that is also integrated with USDA API (third party api that serves nutritional values of foods)',
                        'To be able to maintain and add features to existing projects',
                        'To be able to develop new pages for Shopify projects'
                    ]
                },
                {
                    company: 'Xtendly',
                    position: 'Jr. Web Developer (PHP)',
                    description: 'A digital marketing company. (Philippines)',
                    tenure: {
                        from: 'Aug. 2016',
                        to: 'Mar. 2018'
                    },
                    responsibilities: [
                        'To be able to develop pages for Wordpress projects',
                        'To be able to maintain and fix bugs of an in-house Laravel project',
                        'To be able to develop a Restful API that will serve an in-house mobile app project',
                        'To be able to add new features for the projects assigned'
                    ]
                }
            ]
        }
    }
}
</script>
