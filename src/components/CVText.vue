<template>
  <main class="container-fluid">
    <div class="row d-flex justify-content-center page-content">
      <div class="container">
        <section class="col-sm-10 col-md-10 col-lg-12 rounded-top bg-section13 text-center" id="about">
          <div class=" d-flex justify-content-center pt-3  ">
            <h1> <span class="text-primary ">About me</span></h1>
          </div>
          <hr />
          <div class=" justify-content-center col-sm-2 col-md-10 col-lg-12 ps-5 pe-5">
            <blockquote class="blockquote">
            <p>I am a 21 year old hardworking and ambitious student with great passion,
            working in online/digital services.
            I am currently in my third year of studying Computer Sciences at South
            East European University.
            I have excellent communication skills, enabling me to effectively
            collaborate with a wide range of people. Eager and motivated to
            achieve team objectives and goals. I am seeking a position in the
            industry, in which I can put into practice my knowledge and
            experience. Well-versed in the Office suite,Google Spreadsheets <br />
            and currently studying programming and markup languages such as HTML, CSS,
            Java, C++, Asp .NET, SpringBoot.
            </p>
            </blockquote>
          </div>

           <div v-for="info in PersonalInfoObj" :key="info.title">
          <PersonalInfo
              :classIcon="info.iconClass"
              :title="info.title"
              :description="info.description"
          />
          </div>
         <div>
          <PersonalInfo
              classIcon="fa-wrench"
              title="Skills"
              description="My skills"
          />
          <button @click="isSoftware=true" :disabled="isSoftware">Software Skills</button>
          <button @click="isSoftware=false" :disabled="!isSoftware">Professional skills</button>
          <div v-for="skill in showSkills" :key="skill.nameSkill">
            <p>{{ skill.nameSkill }}</p>
          </div>
        </div>
         </section>

      <section id="education">
       <div class="col-sm-2 col-md-10 col-lg-12 px-2  rounded-top bg-section2 text-center">
        <i class="fa fa-graduation-cap fa-2x py-2" aria-hidden="true"
        >Education</i>
        <div v-for="info in EducationInfoObj" :key="info.title">
          <EducationInfo
              :title="info.title"
              :date="info.date"
              :description="info.description"
          />
        </div>
        <div class="col-sm-7 col-md-10 col-lg-5 rounded-start shadow bg-section13 mx-auto border-1">
          <ProgressBarInfo LanguageName="Albanian(native1)" knowledge="100"/>
          <ProgressBarInfo LanguageName="English" knowledge="80"/>
          <ProgressBarInfo LanguageName="Macedonian" knowledge="75"/>
          <ProgressBarInfo LanguageName="Turkish" knowledge="65"/>

        </div>
        </div>
      </section>
      <section id="experiences">
      <div class="col-sm-2 col-md-10 col-lg-12 px-2  py-5 rounded-top text-center bg-section13">
        <i class="fa fa-user-plus fa-2x py-2" aria-hidden="true">Experiences</i>
        <div v-for="info in ExperienceInfoObj" :key="info.title">
          <EducationInfo
              :title="info.title"
              :date="info.date"
              :description="info.description"
          />
        </div>
      </div>
      </section>
    </div>
    </div>
  </main>
</template>

<style scoped>
</style>

<script>
import ProgressBarInfo from "./ProgressBarInfo.vue";
import PersonalInfo from "./PersonalInfo.vue";
import EducationInfo from "./EducationInfo.vue";

export default {
  components: {
    PersonalInfo,
    EducationInfo,
    ProgressBarInfo,
  },
  data() {
    return {
      PersonalInfoObj: [
        {
          iconClass: "fa-envelope-o",
          title: "E-mail",
          description: "auroratopojani47@gmail.com",
        },
        {
          iconClass: "fa-mobile",
          title: "Phone",
          description: "+389 72 240 047",
        },
        {
          iconClass: "fa-map-marker",
          title: "Address",
          description: "Road 157 number 2, Skopje",
        },
      ],
      EducationInfoObj: [
        {
          title: "Bachelor of Computer Science - SEE University Skopje ",
          date: "2019-2023",
          description: "Computer Science Technology (CST), GPA:9.60",
        },
        {
          title: "High School Diploma – Zef Lush Marku ",
          date: "2015 - 2019",
          description: "Mathemathics, GPA:5.00",
        },
        {
          title: "Kongresi i Manastirit ",
          date: "2006-2015",
          description: "GPA:5.00",
        },
      ],
      ExperienceInfoObj: [
        {
          title: "Youth Education Forum ",
          date: "10.2018 –08.2019",
          description: "Activist & Project Researcher",
        },
        {
          title: "CBC Loja ",
          date: "03.2019 –04.2019",
          description: "Project Volunteer",
        },
        {
          title: "American Corner ",
          date: "04.2019 –06.2019",
          description: "Project Manager",
        },
        {
          title: "Auran Creart ",
          date: "06.2019 –05.2021",
          description: "Co-Founder",
        },
        {
          title: "IPSOS SKOPJE ",
          date: "07.2019-06.2020",
          description: "Survey Research (Assistant Manager)",
        },
        {
          title: "Municipality of Cair",
          date: "30.08.2021-28.09.2021",
          description: "Census Enumerator",
        },
      ],
      Skills: [
        {
          nameSkill: "Team Management",
          type: "GeneralSkill",
        },
        {
          nameSkill: "Leadership & Teamwork",
          type: "GeneralSkill",
        },
        {
          nameSkill: "Problem Solving",
          type: "GeneralSkill",
        },
        {
          nameSkill: "Microsoft Powerpoint",
          type: "GeneralSkill",
        },
        {
          nameSkill: "Microsoft Office Skills",
          type: "SoftwareSkill",
        },
        {
          nameSkill: "MS SQL",
          type: "SoftwareSkill",
        },
        {
          nameSkill: "C++",
          type: "SoftwareSkill",
        },
        {
          nameSkill: "JAVA",
          type: "SoftwareSkill",
        },
        {
          nameSkill: ".NET",
          type: "SoftwareSkill",
        },
        {
          nameSkill: "HTML/CSS",
          type: "SoftwareSkill",
        },


      ],
      isSoftware: true, // if true show the software skill otherwise general skills

    };
  },
  computed: {
    showSkills() {

      if (this.isSoftware)
        return this.Skills.filter(item => item.type === "SoftwareSkill")
      else
        return this.Skills.filter(item => item.type === "GeneralSkill")
    }
  },


};
</script>