<template>
    <div  class="tw-flex tw-flex-row tw-justify-end">
        <ul>
            <li>
                <a href="#intro">Intro</a>
            </li>
            <li>
                <a href="#skills">Skills</a>
            </li>
            <li>
                <a href="#career">Career</a>
            </li>
            <li>
                <a href="#portfolio">Portfolio</a>
            </li>
        </ul>
    </div>  
    
</template>
<script>
export default {
    name: 'Navigation'
}
</script>

<style scoped>
    ul li {
        display:inline-block;
        margin-right: 3rem;
    }

    ul li a {
        color: white;
    }
</style>