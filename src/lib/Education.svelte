<script>
  import mainorLogo from "../assets/mainor.png";
  import evoLogo from "../assets/evolution.png";
  import udemyLogo from "../assets/Udemy.png";
  import valiItLogo from "../assets/vali-it.png";
  import smartworkLogo from "../assets/smartwork.jpeg";
</script>

<div class="container">
  <div class="title">EDUCATION</div>
  <div class="card-style">
    <div class="card">
      <img src={smartworkLogo} alt="Smartwork" class="smartLogo" />
      <h1>Smartwork academy</h1>
      <h3>Present</h3>
      <p>Specialty: Foundations of User Experience UX Design</p>
    </div>
    <div class="card">
      <img src={evoLogo} alt="Evolution Gaming" class="logo" />
      <h1>Evolution Typescript-Bootcamp</h1>
      <h3>January - May 2023</h3>
      <p>
        Specialty: Typescript, React, CSS, Redux, Mobix, Unit test, Babylon,
        Pixi.js
      </p>
    </div>
    <div class="card">
      <img src={udemyLogo} alt="Udemy" class="logo" />
      <h1>Udemy course- The Complete Web Developer in 2022: Zero to Mastery</h1>
      <h3>January - December 2022</h3>
      <p>Specialty: Javascript, React, CSS</p>
    </div>
    <div class="card">
      <img src={valiItLogo} alt="Vali-IT" class="logo" />
      <h1>“Vali IT!”— an adult retraining program</h1>
      <h3>August - November 2018</h3>
      <p>Specialty: Javascript, React, CSS, C#, .NET, SQL</p>
    </div>
    <div class="card">
      <img src={mainorLogo} alt="Mainor" class="mainorLogo" />
      <h1>Estonian Entrepreneurship University of Applied Sciences, Tallinn</h1>
      <h3>September 2009 - June 2012</h3>
      <p>Specialty: entrepreneurship and business management</p>
    </div>
  </div>
</div>

<style>
  .card {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 15px;
    text-align: center;
  }
  .logo {
    width: 100px;
    height: auto;
    padding: 10px;
  }
  .smartLogo {
    width: 130px;
    height: 60px;
    padding: 10px;
  }
  .mainorLogo {
    width: 80px;
    height: 80px;
    padding: 10px;
  }
</style>
