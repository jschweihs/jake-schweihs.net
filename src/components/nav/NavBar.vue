<template>
    <div class="container">
        <div class="nav-bar">
            <div class="nav-header">
                <div class="logo">
                    <a class="logo-anchor" href="/">
                        <img class="logo-img" src="/images/logo.png"/>
                    </a>
                </div>
                <div class="nav-links">
                    <ul class="nav-list">
                        <li class="nav-item">
                            <a href="/">
                                Portfolio
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/">
                                Artwork
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/">
                                Blog
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/">
                                Contact
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
            <h1 class="nav-title">
                Full Stack Web Developer and Artist
            </h1>
            <h3 class="nav-subtitle">
                I strive to create elegant, clean, reusable, and readable code.
            </h3>
        </div>
    </div>
</template>



<style scoped>

    .nav-bar {
        padding: 20px 0;
    }
    .nav-header {
        display: block;
        padding: 20px 0;
    }

    .logo {
        width: 80px;
        height: 80px;
        display: inline-block;
    }

    .logo-anchor {
        padding: 10px;
        display: inline-block;
    }

    .nav-links {
        
        display: inline-block;
        margin-left: 60px;
    }

    .nav-list {
        list-style-type: none;
        margin: 0;
        padding: 0;
    }

    .nav-item {
        float: left;
        display: block;
        text-align: center;
        font-size: 18px;
        margin: 0 12px;
    }

    .nav-item a {
        text-decoration: none;
        color: #4040ff;
        transition: .25s;
    }

    .nav-item a:hover {
        color: orange;
    }

    .navitem li:first-child a { 
        border-left: 10px solid #3498db; 
    }

    .nav-item a:after {
        content: "";
        display: block;
        margin: 0 auto;
        width: 0;
        border-bottom: 1px solid orange;
        transition: all 0.3s ease 0s; 
        -webkit-transition: all 0.3s ease 0s; 
    }

    .nav-item a:hover:after {
        width: 100%;
    }

    .nav-title {
        font-size: 48px;
        text-align: center;
    }

    .nav-subtitle {
        text-align: center;
        font-weight: 100;
        color: #333;
    }

</style>