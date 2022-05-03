<template>
    <main>
        <div class="container">
            <h3>--> content here</h3>
        </div>
    </main>
</template>

<script>
export default {
    name: 'MainComponent'
}
</script>

<style lang="scss" scoped>

    main {
        background-color: black;

        .container {
            padding: 2rem 0;
            
            h3 {
                color: white;
            }
        }
    }

</style>