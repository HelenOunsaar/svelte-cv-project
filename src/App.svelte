<script>
  import { Route, Router } from "svelte-navigator";
  import About from "./lib/About.svelte";
  import Education from "./lib/Education.svelte";
  import Experience from "./lib/Experience.svelte";
  import Skills from "./lib/Skills.svelte";
  import ErrorPage from "./lib/ErrorPage.svelte";
  import Footer from "./component/Footer.svelte";

  import Navbar from "./component/Navbar.svelte";
  import "./global.css";
</script>

<head>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" />
  <link
    href="https://fonts.googleapis.com/css2?family=Poppins:wght@200;500&display=swap"
    rel="stylesheet"
  />
</head>

<Router>
  <div class="main">
    <Navbar />
    <div class="content">
      <Route path="/" component={About} />
      <Route path="/skills" component={Skills} />
      <Route path="/experience" component={Experience} />
      <Route path="/education" component={Education} />
      <Route path="*" component={ErrorPage} />
    </div>
    <Footer/>
  </div>
</Router>
