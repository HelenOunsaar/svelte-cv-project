<script>
  import itkLogo from "../assets/ITK.jpeg";
  import smitLogo from "../assets/smit.png";

  let showITKDetails = false;
  let showSMITDetails = false;

  function toggleITKDetails() {
    showITKDetails = !showITKDetails;
  }

  function toggleSMITDetails() {
    showSMITDetails = !showSMITDetails;
  }

  function handleITKCardKeyPress(event) {
    if (event.key === "Enter") {
      toggleITKDetails();
    }
  }

  function handleSMITCardKeyPress(event) {
    if (event.key === "Enter") {
      toggleSMITDetails();
    }
  }
</script>

<div class="container">
  <div class="title">EXPERIENCE</div>
  <div class="card-style">
    <div class="card-wrapper">
      <div
        class="card"
        on:click={toggleSMITDetails}
        on:keydown={handleSMITCardKeyPress}
      >
        <img src={smitLogo} alt="SMIT" class="smitLogo" />
        <h1>SMIT- IT and development center of the Ministry of the Interior</h1>
        <h2>Frontend developer</h2>
        <h3>September - November 2018</h3>
        {#if showSMITDetails}
          <p>
            Gained practical experience in software development, collaborated
            with a team to develop innovative solutions, demonstrated
            proficiency in CSS, HTML, Javascript, React.
          </p>
        {/if}
      </div>
    </div>
    <div class="card-wrapper">
      <div
        class="card"
        on:click={toggleITKDetails}
        on:keydown={handleITKCardKeyPress}
      >
        <img src={itkLogo} alt="ITK" class="itkLogo" />
        <h1>East Tallinn Central Hospital, Tallinn</h1>
        <h2>Laboratory assistant</h2>
        <h3>May 2013 – June 2018</h3>
        {#if showITKDetails}
          <p>
            Assisted medical staff in various labor-related procedures and
            tasks. Maintained a clean and safe working environment. Registration
            of analyzes, preparation for work.
          </p>
        {/if}
      </div>
    </div>
  </div>
</div>

<style>
  .card {
    padding: 15px;
    cursor: pointer;
    display: flex;
    flex-direction: column;
    align-items: center;
    box-sizing: border-box;
    text-align: center;
    min-height: 290px;
  }

  .card:hover {
    box-shadow: 0 4px 12px 0 rgb(191, 161, 129, 0.5);
  }

  .itkLogo {
    width: 100px;
    height: 70px;
    padding: 5px;
  }

  .smitLogo {
    width: 100px;
    height: 70px;
    padding: 5px;
  }

  @media screen and (max-width: 768px) {
    .container p {
      text-align: justify;
    }
  }
</style>
