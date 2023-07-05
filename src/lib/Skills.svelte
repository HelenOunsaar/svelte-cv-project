<script>
  import SkillsCard from "./SkillsCard.svelte";

  const softSkills = [
    "Research",
    "Self-management",
    "Communication",
    "Teamwork",
    "Problem solving",
    "Adaptability",
    "Attention to detail",
  ];

  const hardSkills = [
    "Software development",
    "Responsive design",
    "Cross-Browser Compatibility",
    "Testing and Debugging",
    "User Interface",
    "Back-end basics",
    "Frameworks and Libraries",
    "Version Control",
  ];

  const programmingSkills = [
    "HTML",
    "CSS",
    "JavaScript",
    "TypeScript",
    "React",
    "Redux",
    "Svelte",
    "Jest",
    "Visual Studio",
    "Github",
  ];

  const certificates = [
    "Evolution Typescript Bootcamp - 2023",
    "Vali-IT adult retraining program - 2018",
  ];

  const language = ["Estonia", "English"];
</script>

<main class="container">
  <div class="card-style">
    <SkillsCard title="Soft Skill" skills={softSkills} />
    <SkillsCard title="Hard Skill" skills={hardSkills} />
    <SkillsCard title="Programming and Development" skills={programmingSkills} />
    <SkillsCard title="Certificates" skills={certificates} />
    <SkillsCard title="Language" skills={language} />
  </div>
</main>

