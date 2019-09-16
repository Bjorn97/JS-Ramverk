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
                <div class="boop">
                        <b-dropdown id="dropdown-1" text="Week" class="m-md-2">
                            <b-dropdown-item>
                                <router-link to="/week">Week1</router-link>
                            </b-dropdown-item>

                            <b-dropdown-item>
                                <router-link to="/week2">Week2</router-link>
                            </b-dropdown-item>
                        </b-dropdown>
                </div>
            </nav>
        </div>
        <div class="about">
            <a href="https://github.com/Bjorn97/JS-Ramverk.git"><h1>Gitrepo</h1></a>
        </div>
        <div class="text">
            <h3>My insperation</h3>
            <p>For the designpattern regarding this weeks assignment i used the open-source designframework bootstrap which provided a clean look to everything.
                It worked extreamely smoothly and i was very happy with the result. However one of the demands on the assignment was that the datepicker were to be of your own making.
                This meant that i could not use bootstraps built in datepicker design but that i had to make my own. I started looking around for easy to make datepickers and found facebooks design.
                It's simple yet elegant so i thought why not try that so with it as insperation i started making a datepicker with 3 boxes one for year one for month and one for day.
                After figuring out how to use forloops in this new framework im learning it all fell into place and even though i would like to make the dropdown menus a bit more styleish
                and fuctional it works for the time that was allocated and the fact that i had to learn allot. The rexex patterns i used could also need improving and if i had more time i
                definetly would improve them. However they do catch most errors without restricting the users inputs too much.
            </p>
        </div>
    </div>
</template>

<script>

</script>


<style>
    .about {
        width: 20%;
        margin: 0 auto;
        text-align: center;
        margin-top: 150px;
        border: 2px solid #8CB5CA;
    }
    .text {
        margin: 0 auto;
        width: 60%;
        margin-top: 100px;
    }
    .text h3 {
        text-align: center;
    }
</style>
