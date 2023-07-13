<script>
export default {
    name: "HeaderComponent",
    data() {
        return {

        }
    },
    methods: {

    }
}
</script>

<template>
    <header>
        
        <section>

                <div class="nav-container">

                    <nav class="col-small">
                        <ul>
                            <li>
                                <a href="#">
                                    <img src="../assets/img/dc-logo.png" alt="logo_Dropbox">
                                </a>
                            </li>
                        </ul>
                        
                    </nav>


                    <nav class="col-big">
                        <ul>
                            <li>
                                <a href="#">Charters</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="#">Comics</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="#">Movies</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="#">TV</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="#">Games</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="#">Collectibles</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="#">Videos</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="#">Fans</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="#">News</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="#">Shop</a>
                            </li>
                        </ul>
                    </nav>
                </div>

        </section>
    </header>
</template>

<style lang="scss" scoped>

.nav-container{
    display: flex;
    justify-content: space-between;
}

header section .nav-container ul {
    display: flex;
    list-style: none;
} 

.col-small{
    display: flex;
}
.col-big{
    display: flex;
    justify-content: center;
    align-items: center;
}

header section .nav-container ul li a{
   color: #787878;
   text-decoration: none;
}
</style>