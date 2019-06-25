<template>
    <div id="app">
        <GeneralInformation/>
        <Education/>
        <ContactInformation/>
    </div>
</template>

<script>
    import GeneralInformation from './components/GeneralInformation';
    import Education from './components/Education';
    import ContactInformation from './components/ContactInformation';

    export default {
        name: 'app',
        components: {GeneralInformation, Education, ContactInformation},
        data() {
            return {
                showWhich: 'GeneralInformation'
            }
        }
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
