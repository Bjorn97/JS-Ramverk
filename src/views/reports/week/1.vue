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
    </div>
</template>

<style>
    .about {
        width: 20%;
        margin: 0 auto;
        text-align: center;
        margin-top: 150px;
        border: 2px solid #8CB5CA;
    }
</style>
