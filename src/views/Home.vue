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
        <div class="content">
            <div class="text">
                <h1>About me</h1>
                <p>
                    Hello im a 22 year old webdeveloping student interested in frontend design and development. I'm from a small town in northern Småland known for swedish style cheesecake and Astrid Lindgren.
                    I play tennis, golf and videogames on my freetime and love to cook as well when i get the opurtunity.
                    <br>
                    I look forward to learning more about js frameworks since ive worked with them before but never vue and never truely indepth so i think this will be facinating.
                </p>
            </div>
            <div class="img">
                <img src="../assets/Me.jpg" alt="hej">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HelloWorld',
    props: {
        msg: String
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
        font-family: 'Montserrat';
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
    .wrapper .content {
        display: flex;
        margin-top: 100px;
    }
    .wrapper .content .text {
        margin-left: 8%;
        padding-left: 2%;
        margin-right: 10%;
        width: 30%;
        border-left: 2px solid #8CB5CA;
        border-right: 2px solid #8CB5CA;
    }

    .wrapper .content .text p {
        margin-top: 70px;
    }

    .wrapper .content .img img {
        width: 500px;
    }
</style>
