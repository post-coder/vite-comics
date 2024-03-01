<script>
export default {
    name: 'AppNav',
}
</script>

<template>

    <nav>
        <div class="container">

            
            <img id="logo" src="/img/dc-logo.png" alt="Logo DC">
            

            <ul class="links">
                    <li>Characters</li>
                    <li class="active">Comics</li>
                    <li>Movies</li>
                    <li>TV</li>
            </ul>
        </div>
    </nav>

</template>

<style lang="scss">
@use '../styles/general' as *;

nav {
    background-color: white;
    color: black;

    height: 120px;

    .container {
        display: flex; 
        justify-content: space-between;
        align-items: center;
        height: 100%;
    }


    #logo {
        height: 80px;
    }

    ul.links {
        display: flex;
        align-items: stretch;
        gap: 50px;

        height: 100%;

        list-style-type: none;

        font-weight: bold;
        text-transform: uppercase;

        margin: 0;

        li {
            position: relative;

            display: flex;
            align-items: center;

            &.active::before {
                content: '';
                position: absolute;
                bottom: 0;
                left: 0;
                
                width: 100%;
                height: 6px;
                background-color: #0282f9;
            }
        }
        
        
    }
}

</style>