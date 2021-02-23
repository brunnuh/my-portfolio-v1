<template>
    <section class="container-section">
        <AboutComponent />
        <SkillsComponent />
    </section>
</template>

<script>
import AboutComponent from './About/index'
import SkillsComponent from './Skills/index'
export default {
    components: {
        AboutComponent,
        SkillsComponent
    }
}
</script>

<style scoped lang="scss">
    .container-section{
        grid-area: BD;
        display: flex;
        flex-direction: column;
        align-items: center;
        //background-color: var(--sv);
    }
</style>