<script>
  import helenImage from "../assets/helen.jpeg";
  export let name = "Helen Õunsaar";
</script>

<div class="container">
  <div>
    <div class="title">ABOUT ME</div>
    <div class="about-style">
      <img src={helenImage} alt="Helen Õunsaar" class="image" />
      <div>
        <p>
          Hello, everyone! My name is {name}, and I am actively seeking a career
          in software development. I bring with me a diverse background, having
          previously worked as a labor assistant at East-Tallinn Central
          Hospital. While I thoroughly enjoyed my time there, my passion for
          technology and coding eventually led me to explore frontend
          development.
        </p>
        <p>
          In 2018, I participated in the Vali-IT course, which provided me with
          a solid foundation in software development. Building upon that
          knowledge, I recently completed the Evolution Typescript Bootcamp from
          January to May 2023. This intensive program equipped me with advanced
          skills in frontend development and a deep understanding of TypeScript.
        </p>
        <p>
          With my combination of practical experience, self-learning, and formal
          training, I am eager to contribute my skills and enthusiasm to a
          software development team. I am always up for a challenge and strive
          to continuously learn and grow in this rapidly evolving field.
        </p>
      </div>
    </div>
  </div>
</div>

<style>
  .about-style {
    display: flex;
    align-items: flex-start;
    margin-top: 50px;
    gap: 20px;
  }

  .image {
    width: 200px;
    height: auto;
    border-radius: 20px;
    padding: 1px;
  }

  .about-style p {
    margin: 0;
    text-align: justify;
    margin-bottom: 10px;
  }

  @media screen and (max-width: 768px) {
    .container {
      text-align: left;
    }

    .about-style {
      flex-direction: column;
      align-items: center;
      margin-top: 10px;
    }

    .image {
      margin-top: 10px;
    }

    .about-style p {
      margin-left: 0;
      margin-top: 20px;
    }
  }
</style>
