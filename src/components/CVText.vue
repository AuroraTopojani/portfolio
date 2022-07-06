<template >
<main class="container-fluid ">
<div class="row">

  <section class="container-fluid" >
  <div class="row align-items-center py-2">
    <div class="col-xl-6 col-bg-6 col-md-6 col-sm-12 text-center "  >
      <img src="../assets/images/Picture2.jpg" alt="icon" width="180px" height="200px" />
    </div>
    <div class="col-xl-6 col-bg-6 col-md-6 col-sm-12 pt-3">
      <h1>Aurora Topojani</h1>
      <h2>Student of CST</h2>
    </div>
  </div>
  </section>

  <section class="container py-2">
    <div class="text-center" >
        <span class="title text-center">About me</span>
    </div>
        <hr width="100%" align="center"/>
    <h5 class="aboutme">I am a 21 year old hardworking and ambitious student with great passion, working in online/digital services.<br>
      I am currently in my third year of studying Computer Sciences at South East European University.
      <br>I have excellent communication skills, enabling me to effectively collaborate with a wide range of people.
      Eager <br>and motivated to achieve team objectives and goals.
      I am seeking a position in the industry, in which <br>I can put into practice my knowledge and experience.
      Well-versed in the Office suite,Google  Spreadsheets <br> and currently studying programming and markup languages such as HTML, CSS, Java, C++, Asp .NET, SpringBoot.
    </h5>
  </section>

  <section >
    <div class="container py-2">
    <div id="leftbox">
      <i class="fa fa-envelope-o fa-2x py-2" aria-hidden="true" >Email</i>
      <h6>auroratopojani47@gmail.com</h6>
      <i class="fa fa-mobile fa-2x py-2" aria-hidden="true">Phone</i>
      <h6>+389 72 240 047</h6>
      <i class="fa fa-map-marker fa-2x py-2" aria-hidden="true">Address</i>
      <h6>Road 157 number 2, Skopje</h6>
    </div>

    <div id="middlebox">

      <i class="fa fa-graduation-cap fa-2x py-2" aria-hidden="true">Education</i>
      <h6> 2015-2019 High School Diploma – Zef Lush Marku</h6>
      <h6>  2019-2023	 Bachelor of Computer Science - SEE University Skopje (Student)</h6>

      <i class="fa fa-language fa-2x py-2" aria-hidden="true">Languages</i>
      <h6>Albanian : Native</h6>
      <h6>Macedonian: Proficient</h6>
      <h6>English: Fluent</h6>

      <i class="fa fa-wrench fa-2x py-2" aria-hidden="true">Skills</i>
      <h6> Team Management</h6>
      <h6> Leadership & Teamwork</h6>
      <h6> Problem Solving </h6>
      <h6> Commuinaction </h6>
    </div>

    <div id="rightbox">

      <i class="fa fa-user-plus fa-2x py-2" aria-hidden="true">Experiences</i>
      <ul>
      <h5>10.2018 –08.2019	Activist & Project Researcher – Youth Education Forum</h5>
      <h5>03.2019 –04.2019	Project Volunteer – CBC Loja</h5>
      <h5>04.2019 –06.2019  Project Manager – American Corner</h5>
      <h5>07.2019-06.2020 Survey Research (Assistant Manager)-IPSOS SKOPJE </h5>
      <h5>30.08.2021-28.09.2021 Census Enumerator -Municipality of Cair</h5>
      </ul>

    </div>
    </div>
  </section>
 </div>
  </main>
</template>

<style scoped>
.align-items-center {border-style: outset; padding:100px; background-color: cadetblue; border-bottom-width: thick; border-radius:20px;}
.container-fluid{background-color:snow}
.aboutme{ text-align: center; font-size: 20px;}
#leftbox {

 padding: 50px;
  float:left;
  background-color: lightgrey;
  width:33%;
  height:500px;
}
#middlebox{
  border-style: inset;
  padding: 50px;
  float:left;
  background-color: darkgrey;
  width:34%;
  height:500px;
}
#rightbox{
  padding: 50px;
  float:right;
  background:lightgrey;
  width:33%;
  height:500px;
}
</style>

<script>
export default {
  data() {
    return {};
  },
};
</script>