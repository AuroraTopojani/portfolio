<template >
  <main class="container-fluid">
    <div class="row d-flex shadow justify-content-center">
      <div class="col-sm-7 col-lg-3 p-5 rounded-top bg-section13">
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

          <div v-for="skill in Skills" :key="skill.nameSkill">
            <p>{{ skill.nameSkill }}</p>
          </div>
        </div>
      </div>

      <div class="col-sm-7 col-lg-3 p-5 shadow rounded-top bg-section2">
        <i class="fa fa-graduation-cap fa-2x py-2" aria-hidden="true"
        >Education</i
        >
        <div v-for="info in EducationInfoObj" :key="info.title">
          <EducationInfo
              :title="info.title"
              :date="info.date"
              :description="info.description"
          />
        </div>
        <div class="col-sm-7 col-lg-12 p-5 rounded-start shadow bg-section13">
          <ProgressBarInfo LanguageName="Albanian(native1)" knowledge="100" />
          <ProgressBarInfo LanguageName="English" knowledge="80" />
          <ProgressBarInfo LanguageName="Macedonian" knowledge="75" />
          <ProgressBarInfo LanguageName="Turkish" knowledge="65" />

        </div>
      </div>

      <div class="col-sm-7 col-lg-3 p-5 shadow rounded-3 bg-section13">
        <i class="fa fa-user-plus fa-2x py-2" aria-hidden="true">Experiences</i>
        <div v-for="info in ExperienceInfoObj" :key="info.title">
          <EducationInfo
              :title="info.title"
              :date="info.date"
              :description="info.description"
          />
        </div>
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


    };
  }
};
</script>