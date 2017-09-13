<template>
<div>
<div class="home has-text-centered">
    <div class="crop">
            <img src="./../assets/aman.jpg" id="displayPic"></img>
    </div>
    <br/>
    <h1 class="title">Aman Jagga</h1>
    <h2 id="designation" class="subtitle">UI/Java developer</h2>
    <p>A developer with 3 years of experience in UI/Java domain and still experimenting with different 
technologies before settling to one. I love the way technology is creating products and solving problems. Apart from technology, finance is the other domain that I am exploring into.</p>
    <br />
    <a href="https://drive.google.com/uc?export=download&id=0B7h4RQvtmeu8MFlZVGVzWWRFRTA">
    <button class="button is-primary is-size-4"><i class="fa fa-download" aria-hidden="true"></i><span>&nbsp;Download my resume</span></button>
    </a>
</div>
<footer class="columns">
    <div class="column">Made in 
        <i class="fa fa-heart" id="heartFont"aria-hidden="true"></i>&nbsp; with Bulma + Vue.js</div>
    <div class="column has-text-centered">
    </div>
        <div class="column has-text-right"><a href="https://legpin.com/resumeV1">Load older version of this app</a></div>
</footer>
</div>
</template>


<script>
export default {
}
</script>


<style scoped>
 #displayPic {
     width: 450px;
     height: 600px;
 }

 .crop {
    width: 17rem;
    height: 18rem;
    overflow: hidden;
    border-radius: 150px;
    border-width: 4px;
    border-color: #00d1b2;
    border-style: solid;
    margin: auto;
 }
 .home {
     margin:auto;
     width:50%;
 }
 #heartFont {
     color:red;
 }
 footer {
    position: fixed;
    bottom: 10px;
    width: 100%;
}
#designation {
    margin-top: -1rem;
}
</style>