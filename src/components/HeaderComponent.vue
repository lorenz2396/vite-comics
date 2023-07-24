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
        <div class="container">
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
                    </div>
    </header>
</template>

<style lang="scss" scoped>

.nav-container{
    display: flex;
    justify-content: space-between;
}

ul {
    display: flex;
    list-style: none;
        li {
            a{
                color: #525552;
                text-decoration: none;
                font-size: .8em;
                
            }
        }
}

.col-small{
    display: flex;
}
.col-big{
    display: flex;
    justify-content: flex-end;
    align-items: center;
}

img{
    width: 80px;
    height: 80px;
    margin-top: 10px;
}
</style>