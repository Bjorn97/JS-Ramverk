<template>
    <div class="wrapper">
        <div class="header">
            <div class="name">
                <h1>Björn Andersson</h1>
            </div>
            <nav>
            <div class="link">
                <div class="b">
                    <router-link to="/">Home</router-link>
                </div>

            </div>
                <div class="link boop">
                    <div class="b">
                        <router-link to="/week">Week</router-link>
                    </div>
                </div>
            </nav>
        </div>
        <div class="about">
            <a href="https://github.com/Bjorn97/JS-Ramverk.git"><h1>Gitrepo</h1></a>
        </div>
    </div>
</template>

<style scoped>
.wrapper {
    width: 100%;
}
.boop {
    margin-left: 5%;
}
.wrapper .header {
    width: 100%;
    display: flex;
}
.wrapper .header .name {
    width: 30%;
    text-align: center;
}
 .wrapper .header nav {
    width: 70%;
    display: flex;
    justify-content: center;
}
.wrapper .header nav .link {
    width: 15%;
    text-align: center;
    border-top: 2px solid #8CB5CA;
    border-bottom: 2px solid #8CB5CA;
}
.wrapper .header nav .link:hover {
    transition: background-color 0.8s ease;
    background-color: #8CB5CA;
}
.wrapper .header nav .link .b {
    margin-top: 15px;
    font-size: 2em;
}
.wrapper .header nav .link a {
    text-decoration: none;
    color: #000;
    padding: 20px 0 20px 0;
}
.wrapper .header nav .link a h2 {
    margin: 0;
}
.about {
    width: 20%;
    margin: 0 auto;
    text-align: center;
    margin-top: 150px;
    border: 2px solid #8CB5CA;
}
</style>
